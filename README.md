# Python Automated Billing

This Python script automates the process of logging into an account and submitting a payment using Selenium WebDriver. It also sends notifications via email and SMS regarding the payment status.

## Features

- Automated login to a specified account.
- Submission of payment details including card information.
- Validation of payment amount.
- Email and SMS notifications for successful or failed payments.
- Logging of important events and errors.

## Requirements

To run this script, you need the following:

- Python 3.x
- Selenium
- `python-dotenv` for environment variable management
- A Gmail account for sending email notifications (with "Allow less secure apps" enabled or use an App Password)
- Chrome WebDriver compatible with your Chrome browser version

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/python-automated-billing.git
   cd python-automated-billing
   ```

2. **Install required packages:**

   You can install the required packages using pip:

   ```bash
   pip install selenium python-dotenv
   ```

3. **Download Chrome WebDriver:**

   Download the Chrome WebDriver from [ChromeDriver downloads](https://sites.google.com/chromium.org/driver/) and place it in the `chromedriver-win64` directory within your project folder.

4. **Set up environment variables:**

   Create a `.env` file in the root of your project directory with the following variables:

   ```plaintext
   LOGIN_PAGE=https://example.com/login
   ACCOUNT_NUMBER=your_account_number
   LAST_NAME=your_last_name
   CARD_NUM=your_card_number
   CARD_MONTH=your_card_expiry_month
   CARD_YEAR=your_card_expiry_year
   CARD_CVV=your_card_cvv
   PHONE_NUM=your_phone_number
   APP_PASSWORD=your_gmail_app_password
   ```

## Usage

1. **Run the script:**

   You can run the script from the command line:

   ```bash
   python main.py
   ```

2. **Debugging Mode:**

   To enable debugging mode (which keeps the browser open after execution), set `debugging = True` in the script.

## Logging

The script logs important events and errors to an in-memory string stream. You can print these logs to the console if debugging is enabled or send them via email.

## Notes

- Make sure to handle sensitive information carefully, especially when dealing with payment details.
- Adjust the timeout settings in the `wait_for_element` function if necessary to suit your internet speed.
- The script currently uses Gmail for sending notifications; you may need to adjust SMTP settings if using a different email provider.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

[Dishant Sharma](https://github.com/sharmadishant04)
