pdf:
	pandoc report.md --toc \
	-V toc-title='Table of contents' \
    -V linkcolor:blue \
    -V geometry:a4paper \
    -V geometry:margin=2cm \
	--latex-engine=xelatex -o report.pdf && okular report.pdf
html:
	pandoc -s report.md \
    -V linkcolor:blue \
	-H header.html \
	--metadata title="pyStock report" \
	-o report.md.html
htmltopdf: html
	wkhtmltopdf report.md.html report.pdf
