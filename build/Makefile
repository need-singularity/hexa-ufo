# hexa-ufo — pandoc PDF rebuild for the 4 in-tree pillar specs (Stage-4~7).
#
# Generates 4 pillar PDFs from the canonical .md sources via pandoc +
# xelatex. PDFs land in build/out/ and are .gitignore'd via project root
# .gitignore. Stage-1/2/3 substrates live in sister repos (hexa-rtsc /
# hexa-fusion / hexa-antimatter) and have their own build/ infrastructure.
#
# Usage:
#   make -C build check        # verify pandoc + xelatex available
#   make -C build all          # build all 4 pillar PDFs (warp/wormhole/dimjump/dimuse)
#   make -C build warp         # warp pillar only
#   make -C build wormhole     # wormhole pillar only
#   make -C build dimjump      # dimjump pillar only
#   make -C build dimuse       # dimuse composite pillar only
#   make -C build atlas        # main UFO atlas PDF (1890 LOC)
#   make -C build verify       # run `hexa-ufo verify` (cross-link gate)
#   make -C build clean        # remove build artifacts
#   make -C build size         # PDF size summary

ROOT     := ..
OUT      := out
PANDOC   := pandoc
HEADER   := header.tex
HEXA     := $(HOME)/.hx/packages/hexa/hexa.real

# CJK-aware xelatex pipeline. The header.tex include is soft-guarded —
# missing optional packages (xeCJK, titlesec) silently skip. Build host
# without a CJK font still produces a clean ASCII-only PDF.
PANDOC_FLAGS := \
  --pdf-engine=xelatex \
  --variable=geometry:a4paper,margin=25mm \
  --variable=fontsize:11pt \
  --variable=colorlinks:true \
  --variable=linkcolor:black \
  --variable=urlcolor:blue \
  --syntax-highlighting=tango \
  --toc \
  --toc-depth=2

ifneq ($(wildcard $(HEADER)),)
  PANDOC_FLAGS += --include-in-header=$(HEADER)
endif

PDF_WARP     := $(OUT)/hexa-warp.pdf
PDF_WORMHOLE := $(OUT)/hexa-wormhole.pdf
PDF_DIMJUMP  := $(OUT)/hexa-dimjump.pdf
PDF_DIMUSE   := $(OUT)/hexa-dimuse.pdf
PDF_ATLAS    := $(OUT)/hexa-ufo.pdf

PDFS := $(PDF_WARP) $(PDF_WORMHOLE) $(PDF_DIMJUMP) $(PDF_DIMUSE) $(PDF_ATLAS)

.PHONY: all clean check size warp wormhole dimjump dimuse atlas verify

all: $(PDFS)

warp:     $(PDF_WARP)
wormhole: $(PDF_WORMHOLE)
dimjump:  $(PDF_DIMJUMP)
dimuse:   $(PDF_DIMUSE)
atlas:    $(PDF_ATLAS)

$(OUT):
	mkdir -p $(OUT)

$(PDF_WARP): $(ROOT)/warp/hexa-warp.md | $(OUT)
	$(PANDOC) $(PANDOC_FLAGS) \
	  --metadata=title:"hexa-warp — Stage-4 Alcubierre warp metric n=6 encoding (BT-347)" \
	  --metadata=date:"2026-05-09" \
	  -o $@ $<

$(PDF_WORMHOLE): $(ROOT)/wormhole/hexa-wormhole.md | $(OUT)
	$(PANDOC) $(PANDOC_FLAGS) \
	  --metadata=title:"hexa-wormhole — Stage-5 Morris-Thorne traversable wormhole" \
	  --metadata=date:"2026-05-09" \
	  -o $@ $<

$(PDF_DIMJUMP): $(ROOT)/dimjump/hexa-dimjump.md | $(OUT)
	$(PANDOC) $(PANDOC_FLAGS) \
	  --metadata=title:"hexa-dimjump — Stage-6 Calabi-Yau / Kaluza-Klein 4D→26D (BT-348)" \
	  --metadata=date:"2026-05-09" \
	  -o $@ $<

$(PDF_DIMUSE): $(ROOT)/dimuse/hexa-dimuse.md | $(OUT)
	$(PANDOC) $(PANDOC_FLAGS) \
	  --metadata=title:"hexa-dimuse — Stage-7 composite warp+dimjump (BT-349)" \
	  --metadata=date:"2026-05-09" \
	  -o $@ $<

$(PDF_ATLAS): $(ROOT)/ufo/doc/hexa-ufo.md | $(OUT)
	$(PANDOC) $(PANDOC_FLAGS) \
	  --metadata=title:"hexa-ufo — UFO Substrate Atlas + 7-stage Propulsion (1890 LOC)" \
	  --metadata=date:"2026-05-09" \
	  -o $@ $<

# Cross-link to the verify pipeline. `make verify` runs the full
# hexa-ufo n=6 audit; useful pre-PDF as a regression gate.
verify:
	@echo "[build] running: hexa-ufo verify (run_all aggregate)"
	@HEXA_UFO_ROOT=$(realpath $(ROOT)) $(HEXA) run $(ROOT)/cli/hexa-ufo.hexa verify

clean:
	rm -rf $(OUT)

size: $(PDFS)
	@du -h $(PDFS)

check:
	@command -v $(PANDOC) >/dev/null 2>&1 || { echo "MISSING: pandoc";  exit 1; }
	@command -v xelatex   >/dev/null 2>&1 || { echo "MISSING: xelatex"; exit 1; }
	@test -x $(HEXA) || { echo "MISSING: $(HEXA) (install via hx install)"; exit 1; }
	@$(PANDOC) --version | head -1
	@xelatex --version | head -1
	@$(HEXA) --version 2>/dev/null | head -1 || echo "(hexa.real version probe skipped)"
	@echo "OK: build toolchain ready"
