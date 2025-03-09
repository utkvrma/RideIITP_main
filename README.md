# RideIITP - Campus Ride Sharing App

<div align="center">
  <div>
    <img src="https://img.shields.io/badge/-React_Native-black?style=for-the-badge&logoColor=white&logo=react&color=61DAFB" alt="reactnative" />
    <img src="https://img.shields.io/badge/-PostgreSQL-black?style=for-the-badge&logoColor=white&logo=postgresql&color=4169E1" alt="postgresql" />
    <img src="https://img.shields.io/badge/-Expo-black?style=for-the-badge&logoColor=white&logo=expo&color=000020" alt="expo" />
    <img src="https://img.shields.io/badge/-Stripe-black?style=for-the-badge&logoColor=white&logo=stripe&color=008CDD" alt="stripe" />
  </div>
</div>

## Table of Contents

1. [Introduction](#introduction)
2. [Tech Stack](#tech-stack)
3. [Features](#features)
4. [Project Structure](#project-structure)
5. [Setup and Installation](#setup)
6. [Environment Variables](#environment)

## Introduction

RideIITP is a modern ride-sharing application specifically designed for the IIT Patna campus community. Built with React Native and powered by real-time location tracking, the app provides an efficient and user-friendly solution for students and faculty to share rides within and around the campus. Currently running as a local development project.

## Tech Stack

- **Frontend**: React Native with Expo
- **Styling**: TailwindCSS (via NativeWind)
- **State Management**: Zustand
- **Maps**: React Native Maps with Google Maps integration
- **Authentication**: Clerk (local development)
- **Database**: Local PostgreSQL instance
- **Payments**: Stripe (test mode)
- **Language**: TypeScript

## Features

- **Real-time Location Tracking**: Live tracking of rides with Google Maps integration
- **Secure Authentication**: Email/password and Google OAuth sign-in options (development mode)
- **Smart Route Planning**: Intelligent route calculation and fare estimation
- **Digital Payments**: Secure payment processing through Stripe (test mode)
- **Ride History**: Detailed history of past rides
- **Profile Management**: User profile customization and settings
- **Multi-platform**: Works seamlessly on both Android and iOS emulators

## Project Structure

```
RideIITP_main/
├── app/                    # Main application code
│   ├── (api)/             # API routes
│   ├── (auth)/            # Authentication screens
│   └── (root)/            # Main app screens
├── components/            # Reusable React components
├── store/                # State management (Zustand)
├── constants/            # App constants and configurations
├── assets/              # Images, fonts, and other static files
├── types/               # TypeScript type definitions
└── lib/                 # Utility functions and helpers
```

## Setup and Installation

1. Clone the repository:
```bash
git clone https://github.com/utkvrma/RideIITP.git
cd RideIITP
```

2. Install dependencies:
```bash
npm install
```

3. Set up local PostgreSQL database:
   - Install PostgreSQL on your machine
   - Create a new database for the project
   - Run the schema migrations (provided in the `database` folder)

4. Start the development server:
```bash
npx expo start
```

5. Run on emulator or device:
   - Press 'a' for Android emulator
   - Press 'i' for iOS simulator
   - Scan QR code with Expo Go app for physical device (must be on same network)

## Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
# Development mode keys only
EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_...
EXPO_PUBLIC_PLACES_API_KEY=your_google_places_api_key
EXPO_PUBLIC_DIRECTIONS_API_KEY=your_google_directions_api_key
DATABASE_URL=postgresql://localhost:5432/rideittp
EXPO_PUBLIC_SERVER_URL=http://localhost:3000
EXPO_PUBLIC_GEOAPIFY_API_KEY=your_geoapify_key
EXPO_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_...
STRIPE_SECRET_KEY=sk_test_...
```

Note: All API keys should be in test/development mode. Do not use production keys in this local setup.

## Local Development

1. The app runs entirely on your local machine
2. Database is hosted on your local PostgreSQL instance
3. Authentication runs in development mode
4. Payments use Stripe test mode
5. Maps and location services require valid API keys but run in development mode

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.