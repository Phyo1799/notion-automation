# Notion Automation

A Flask application that automates expense tracking in Notion by parsing SMS messages.

## Features

- SMS message parsing for expense tracking
- Integration with Notion API
- User authentication
- QR code generation for easy access
- CSV export functionality

## Local Development Setup

1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Copy `.env.example` to `.env` and fill in your values
5. Run the application:
   ```bash
   python app.py
   ```

## Vercel Deployment

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Login to Vercel:
   ```bash
   vercel login
   ```

3. Deploy to Vercel:
   ```bash
   vercel
   ```

4. Set up environment variables in Vercel:
   - Go to your project settings in Vercel
   - Add the following environment variables:
     - NOTION_API_KEY
     - DATABASE_ID
     - SECRET_KEY
     - ADMIN_EMAIL
     - ADMIN_PASSWORD

## Environment Variables

- `NOTION_API_KEY`: Your Notion API key
- `DATABASE_ID`: Your Notion database ID
- `SECRET_KEY`: Flask secret key for session management
- `ADMIN_EMAIL`: Admin user email
- `ADMIN_PASSWORD`: Admin user password
- `SSL_CERTIFICATE`: (Optional) Path to SSL certificate
- `SSL_KEY`: (Optional) Path to SSL key

## API Endpoints

- `/`: Home page
- `/login`: Login page
- `/logout`: Logout endpoint
- `/qr`: Generate QR code for the current URL
- `/send_sms`: Process SMS messages
- `/export`: Export data to CSV
- `/test_parse`: Test SMS parsing
- `/delete_entry`: Delete a Notion entry

## Security Notes

- Always use HTTPS in production
- Keep your environment variables secure
- Regularly update dependencies
- Use strong passwords for admin accounts

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request
