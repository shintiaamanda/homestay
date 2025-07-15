# Homestay Booking App

A Flutter application for booking homestays with a beautiful and modern UI.

## Features

- **User Authentication**: Login and registration functionality
- **Homestay Listing**: Browse available homestays with detailed information
- **Booking System**: Make reservations with date selection and room quantity
- **Payment Processing**: Multiple payment methods (QRIS, Transfer, Cash)
- **User Profile**: Manage user information and view booking history
- **Modern UI**: Beautiful Material Design 3 interface

## Project Structure

```
lib/
├── models/
│   ├── user_model.dart
│   ├── homestay_model.dart
│   ├── booking_model.dart
│   └── payment_model.dart
├── screens/
│   ├── login_screen.dart
│   ├── register_screen.dart
│   ├── home_screen.dart
│   ├── homestay_detail.dart
│   ├── booking_form.dart
│   ├── payment_screen.dart
│   └── profile_screen.dart
├── services/
│   └── api_service.dart
├── widgets/
│   └── homestay_card.dart
└── main.dart
```

## Getting Started

### Prerequisites

- Flutter SDK (^3.8.1)
- Dart SDK
- Android Studio / VS Code
- Android Emulator or Physical Device

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd homestay
```

2. Install dependencies:
```bash
flutter pub get
```

3. Run the app:
```bash
flutter run
```

## Backend Integration

This app is designed to work with a Laravel backend. The API service expects the following endpoints:

### Base URL
```
http://localhost:8000/api
```

### Required Endpoints

#### Authentication
- `POST /login` - User login
- `POST /users` - User registration

#### Homestays
- `GET /homestays` - Get all homestays
- `GET /homestays/{id}` - Get specific homestay

#### Bookings
- `GET /bookings` - Get all bookings
- `POST /bookings` - Create new booking
- `GET /bookings/{id}` - Get specific booking

#### Payments
- `GET /payments` - Get all payments
- `POST /payments` - Create new payment
- `GET /payments/{id}` - Get specific payment

## Features in Detail

### 1. User Authentication
- Login with email and password
- Registration with name, email, and password
- Form validation and error handling

### 2. Homestay Browsing
- List all available homestays
- Detailed homestay information
- Price calculation and room availability

### 3. Booking System
- Date selection (check-in and check-out)
- Room quantity selection
- Late arrival penalty calculation (10% per day)
- Booking notes and special requests

### 4. Payment Processing
- Multiple payment methods:
  - QRIS
  - Bank Transfer
  - Cash
- Payment confirmation and receipt

### 5. User Profile
- User information display
- Booking history (planned feature)
- Payment history (planned feature)
- App settings and help

## Dependencies

- `flutter`: Core Flutter framework
- `http`: ^1.1.0 - For API HTTP requests
- `cupertino_icons`: ^1.0.8 - iOS style icons

## Development

### Adding New Features

1. Create models in `lib/models/`
2. Add API endpoints in `lib/services/api_service.dart`
3. Create screens in `lib/screens/`
4. Add widgets in `lib/widgets/`
5. Update navigation in main.dart

### Code Style

- Follow Flutter/Dart conventions
- Use meaningful variable and function names
- Add comments for complex logic
- Implement proper error handling

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support and questions, please contact the development team.
