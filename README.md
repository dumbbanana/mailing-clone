# automate

### Pre-requisite

-   Python must be installed in the system.
-   `python --version` should yield an output.
    That indicates that Python is properly installed.
-   Creating a virtual environment to install the required packages.

    ```
    python -m pip install -r requirements.txt
    ```

-   More info on the same can be found [here](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/).
-   Activating the virtual environment.

---

### split_it.py

#### Requirements

-   1 CSV file with Names and Email Addresses
-   1 PDF file which has all the certificates in the above order.
    i.e. The names order in the PDF should be same as that of the
    CSV file.

### Execution

-   Have the PDF with multiple certificates in the same directory
    as that of the `split_it.py` file.
-   Run this command in the terminal

```
python split_it.py
```

-   The above command will generate separate PDF files for each student
    with their name as the file name.

---

### send_mails.py

#### Requirements

-   1 CSV file with Names and Email Addresses
-   PDF files which has the certificate of student in the above order.
    i.e. For every name in the CSV file, there should be a PDF file.

### Execution

-   Have the PDFs of the individual certificates in the same directory
    as that of the `send_mails.py` file.
-   Run this command in the terminal

```
python send_mails.py
```

-   The above command will:
    -   Read name and email ID from the CSV file
    -   Add the HTML content given in the `template.html` as the mail content
    -   Attach the appropriate certificate to that mail
    -   Send the mails to all the students.

---

### PDF_links.txt

- This text file containts a google script to save share links of pdf files in a google drive to a spreadsheet

#### Requirements

-   1 CSV file with Names and Email Addresses
-   1 Google drive folder of PDF files which has all the certificates in the above order.
    i.e. The names order in the PDF should be same as that of the
    CSV file.

### Execution

-  Copy the folder ID which contains the PDF files
-   Open a new CSV file in google sheets in the same folder
-   Paste the google scripts in `Exections -> AppScript`
-   Run the function
-   Links for PDF files with view permission will be generated in order in the google sheet.
 

