 PDF07=docs/jlpt-n4/jlpt-n4-2024-07.pdf PDF12=docs/jlpt-n4/jlpt-n4-2024-12.pdf

all: $(PDF07) $(PDF12)

$(PDF07): manuscript/07/index.md mkdir -p docs/jlpt-n4 pandoc $< -o $@ --pdf-engine=xelatex
-V mainfont="Noto Serif JP" -V sansfont="Noto Sans JP"
--toc --toc-depth=3 -V geometry:margin=1in
--metadata title="JLPT N4 2024/07 題本（不含答案）"

$(PDF12): manuscript/12/index.md pandoc $< -o $@ --pdf-engine=xelatex
-V mainfont="Noto Serif JP" -V sansfont="Noto Sans JP"
--toc --toc-depth=3 -V geometry:margin=1in
--metadata title="JLPT N4 2024/12 題本（不含答案）"

clean: rm -f $(PDF07) $(PDF12)
