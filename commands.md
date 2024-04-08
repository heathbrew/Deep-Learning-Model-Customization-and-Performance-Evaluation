## Document Conversion

### Installing Required Packages

For converting Jupyter notebooks to PDFs or reducing PDF file size, install the necessary packages:

```bash
sudo apt-get update
sudo apt-get install texlive-xetex texlive-fonts-recommended texlive-plain-generic pandoc
sudo apt install ghostscript
```

### Converting Jupyter Notebooks to PDF

```bash
jupyter nbconvert --to pdf 01_data_ingestion_03_data_transformation.ipynb
jupyter nbconvert --to pdf 07_model_evaluation.ipynb
```

These commands convert the specified Jupyter notebooks to PDF format, suitable for reporting or documentation purposes.

### Compressing PDF Files

For compressing PDF files to reduce their file size (while maintaining readability):

```bash
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/screen -dNOPAUSE -dQUIET -dBATCH -sOutputFile=compressed_output.pdf original.pdf
```

Replace `original.pdf` with the name of your PDF file and `compressed_output.pdf` with the desired output file name.

This documentation provides a comprehensive guide to managing datasets, version control, and document conversion within ML projects. By following these practices, teams can ensure efficient data handling, maintain code integrity, and produce high-quality documentation.