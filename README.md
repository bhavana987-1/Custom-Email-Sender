# Custom-Email-Sender

## Features

- Single and Multiple Email Sending: Choose between sending an email to a single recipient or multiple recipients by uploading an Excel file.
- Attachment Support: Add attachments (images or other files) to the email.
- Speech-to-Text Integration: Use speech recognition to compose the email body using voice input.
- Save Email Credentials: Save sender email credentials securely for future use.
- Real-Time Status Updates: Track the status of email delivery with live updates on the total, sent, left, and failed emails.
- User-Friendly GUI: Intuitive interface with buttons for browsing files, attaching files, and sending emails.

## Prerequisites

- Python 3.x
- Python Libraries:
  - `tkinter`: For the GUI.
  - `pygame`: For audio playback.
  - `speech_recognition`: For speech-to-text conversion.
  - `smtplib`: For sending emails.
  - `pandas`: For reading Excel files.
  - `openpyxl` and `xlrd`: For Excel file handling.
  - `Pillow`: For handling image attachments.

To install the necessary Python libraries, run:

```bash
pip install pygame speechrecognition pandas openpyxl xlrd pillow
```

## How to Run

1. Save Email Credentials:
   - Click on the **Settings** button to enter and save your email credentials (Email and Password).
   - Ensure you allow less secure apps or app-specific password for Gmail.

2. Choose Email Sending Mode:
   - Single: For sending an email to a single recipient.
   - Multiple: For sending emails to multiple recipients using an Excel file containing an "Email" column.

3. Compose and Send Email:
   - Enter the recipient email (for single mode) or browse and upload the Excel file (for multiple mode).
   - Add a subject and compose your email.
   - Optionally, click on the Speak button to use voice input for the email body.
   - Attach any files using the **Attachment** button.
   - Click the **Send** button to send the email.

4. **Track Status**:
   - View the status of email delivery (total, sent, left, and failed) at the bottom of the GUI.

## Excel File Format

For multiple email sending, the Excel file must contain an "Email" column with valid email addresses.

Example:

name       email
Bhavana    bhavanabaday@gmail.com

## Error Handling

- Invalid or missing Excel file: An error message is shown if the selected file is not supported.
- Missing required fields: An error message appears if any required field (recipient email, subject, or body) is empty.
- Failed email delivery: The application tracks and reports failed email deliveries.

## Technologies Used

- Python: Programming language.
- Tkinter: GUI library for desktop application development.
- Pandas: Data analysis and manipulation library.
- SMTP (smtplib): Email sending protocol.
- Pillow: Python Imaging Library for handling image attachments.
- Speech Recognition: Converts voice input to text.

## Limitations

- This application uses Gmail's SMTP server (`smtp.gmail.com`), which requires allowing less secure apps or using an app-specific password.
- The email credentials are stored in plain text in the `credentials.txt` file, which is not secure for production use.

## Acknowledgements

- Tkinter: For providing a simple and easy-to-use GUI framework.
- SpeechRecognition: For enabling voice input functionality.
- Pandas: For simplifying Excel file handling.
- SMTP: For enabling email sending functionality.

