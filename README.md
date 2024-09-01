# Mail Merger Script 📧

This Python script automates the process of creating personalized mail content for multiple recipients. It reads a list of recipient names from `names.txt` and merges each name with the body of the mail from `body.txt`. The resulting personalized mail content is saved as individual `.txt` files for each recipient.

## Features
- **Automated Mail Merging**: Generates personalized mail for each recipient.
- **Simple Input/Output**: Reads recipient names from `names.txt` and the mail body from `body.txt`.
- **File Output**: Creates a separate `.txt` file for each recipient containing the personalized mail.

## Getting Started

### Prerequisites
- Python 3.x

### Usage
1. **Prepare the Input Files**:
   - **names.txt**: This file should contain the names of the recipients, one per line.
   - **body.txt**: This file should contain the body of the mail that will be sent to each recipient.

2. **Run the Script**:
   Place the script in the same directory as `names.txt` and `body.txt`. Run the script, and it will generate individual `.txt` files for each recipient.

### Example
```python
# Python program to mail merge
# Names are in the file names.txt
# Body of the mail is in body.txt

# open names.txt for reading
with open("names.txt", 'r', encoding='utf-8') as names_file:

    # open body.txt for reading
    with open("body.txt", 'r', encoding='utf-8') as body_file:

        # read the entire content of the body
        body = body_file.read()

        # iterate over names
        for name in names_file:
            mail = "Hello " + name.strip() + "\n" + body

            # write the mails to individual files
            with open(name.strip() + ".txt", 'w', encoding='utf-8') as mail_file:
                mail_file.write(mail)
```
### Output
For each name in names.txt, the script generates a .txt file containing the personalized mail. The files are named after each recipient.

