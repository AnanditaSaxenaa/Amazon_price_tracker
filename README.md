# Amazon Price Tracker

This script tracks the price of a product on Amazon and sends an email alert if the price drops below a specified threshold.

## Features
- Scrapes the product price from an Amazon page.
- Sends an email alert when the price falls below the desired amount.
- Uses environment variables for sensitive information (SMTP details, email credentials).

## Prerequisites
- Python 3.x
- An SMTP email account (e.g., Gmail, Outlook)
- A `.env` file to store sensitive credentials
- Required Python packages:
  - `requests`
  - `beautifulsoup4`
  - `smtplib`
  - `dotenv`

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/amazon-price-tracker.git
   cd amazon-price-tracker
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Create a `.env` file in the project directory and add your email credentials:
   ```env
   SMTP_ADDRESS=smtp.yourmail.com
   EMAIL_ADDRESS=your-email@example.com
   EMAIL_PASSWORD=your-email-password
   ```

## Usage
1. Open `amazon_price_tracker.py` and set:
   - The `url` variable to the Amazon product page URL.
   - The `BUY_PRICE` variable to your target price.
2. Run the script:
   ```bash
   python amazon_price_tracker.py
   ```
3. If the price drops below the target, an email alert will be sent.

## Notes
- Ensure your email provider allows SMTP access.
- Amazon may block frequent scraping; consider using proxies or delaying requests.
- Modify the `User-Agent` string if necessary to avoid being blocked.

## License
This project is licensed under the MIT License.

## Author
Anandita Saxena

