# Bus Booking USSD Application

A USSD and SMS-based bus booking system for Rwanda, developed using PHP and Africa's Talking API.

## Developers
- TUYIZERE JANVIER
- MUKARUKUNDO SOPHIE

## Features
- View available bus routes in Rwanda
- Select departure date from a list
- Choose a seat
- Confirm booking
- Receive SMS confirmation
- View booking history with SMS notification

## Technical Requirements
- PHP 7.0 or higher
- MySQL 5.6 or higher
- Africa's Talking Account
- Web server (Apache/Nginx)
- Composer (for Africa's Talking SDK)

## Project Setup

1. **Clone the repository**
```bash
git clone [your-repository-url]
cd BusBookingUSSD
```

2. **Install dependencies**
```bash
composer install
```

3. **Database Setup**
- Create a MySQL database named `bus_booking`
- Import the database schema:
```bash
mysql -u root -p bus_booking < database.sql
```

4. **Configuration**
- Update database credentials in `config.php`
- Update Africa's Talking credentials in `send_sms.php`

5. **Africa's Talking Setup**
- Log in to your Africa's Talking account
- Create a new USSD service
- Set the callback URL to your server's URL (e.g., `https://yourdomain.com/ussd.php`)
- Note down the service code

## Project Structure
```
BusBookingUSSD/
├── config.php           # Database configuration
├── ussd.php            # Main USSD handler
├── send_sms.php        # SMS notification handler
├── database.sql        # Database schema
├── vendor/            # Composer dependencies
└── README.md          # Project documentation
```

## Testing
1. **Using Africa's Talking Simulator:**
   - Dial your USSD service code
   - Follow the menu prompts to test the booking flow

2. **Using a real phone:**
   - Dial your USSD service code
   - Follow the menu prompts to make a booking

## Available Routes
- Kigali to Huye
- Kigali to Musanze
- Kigali to Rubavu
- Nyanza to Nyamata
- Kigali to Rusizi

## Security Considerations
- Input validation implemented
- Database queries use prepared statements
- API keys stored securely
- HTTPS recommended for production

## Support
For support, please contact:
- TUYIZERE JANVIER
- MUKARUKUNDO SOPHIE 