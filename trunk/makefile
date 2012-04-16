# Escaneo de archivo de fuente del pdf
SOURCE := ./tex/main.tex

# Prepara la estructura de directorios para la compilación
prepare:
	@echo ' '
	@echo ' '
	@echo '*******************************************************'
	@echo 'PREPARE'
	@echo '*******************************************************'
	@echo 'Creating output folder'
	-mkdir build
	@echo 'Done'
	@echo ' '
	@echo ' '

generate: prepare
	@echo ' '
	@echo ' '
	@echo '*******************************************************'
	@echo 'GENERATE'
	@echo '*******************************************************'
	@echo 'Running the pdflatex utility to generate indexes'
	pdflatex --output-directory build $(SOURCE)
	@echo ' '
	@echo ' '
	@echo 'Done'
	@echo 'Running the pdflatex utility to update references'
	pdflatex --output-directory build $(SOURCE)
	@echo ' '
	@echo ' '
	@echo 'Done'
	@echo 'Running the pdflatex utility to generate pdf'
	pdflatex --output-directory build $(SOURCE)
	@echo ' '
	@echo ' '
	@echo 'Done'
	@echo ' '
	@echo ' '

preview: generate
	@echo ' '
	@echo ' '
	@echo '*******************************************************'
	@echo 'ALL'
	@echo '*******************************************************'
	@echo 'Previewing the pdf'
	-evince ./build/*.pdf &
	@echo 'Done'
	@echo ' '
	@echo ' '

clean:
	@echo ' '
	@echo ' '
	@echo '*******************************************************'
	@echo 'CLEAN'
	@echo '*******************************************************'
	@echo 'Cleaning generated files'
	rm -rf build
	@echo 'Done'
	@echo ' '
	@echo ' '

