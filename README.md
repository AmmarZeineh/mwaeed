# Mwaeed — Service Booking App

A Flutter app that connects **clients with service providers**. Clients browse categories and providers,
book an appointment, pay by card with **Stripe**, and rate the service afterwards.
Available in Arabic (RTL) and English.

![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?logo=dart&logoColor=white)
![Stripe](https://img.shields.io/badge/Payments-Stripe-635BFF?logo=stripe&logoColor=white)
![BLoC](https://img.shields.io/badge/State-BLoC%2FCubit-blue)
![Clean Architecture](https://img.shields.io/badge/Architecture-Clean-success)

<!-- Screenshots: add images to docs/screenshots/ and list them here, e.g.
<p align="center"><img src="docs/screenshots/home.png" width="230"> <img src="docs/screenshots/booking.png" width="230"></p>
-->

## Highlights

- **End-to-end booking flow:** browse → provider details → pick a date and time slot → pay with Stripe → appointment list.
- **Full auth:** sign up, email verification code, log in, forgot and reset password.
- **Clean Architecture per feature** (data / domain / presentation) with **10 feature modules** and dependency injection.
- **Push notifications** with Firebase Messaging and local notifications.
- **Arabic (RTL) and English** with `easy_localization`.

## Features

| Feature | Details |
|---|---|
| Onboarding | First-run walkthrough |
| Auth | Sign up, verification code, log in, forgot / reset password |
| Home | Categories and service providers |
| Search | Search with filters and search types |
| Booking | Provider details and reviews, calendar slot picking (`table_calendar`), booking |
| Payment | Stripe card payment, appointments list |
| Favorites | Save providers |
| Rating | Add, edit and delete ratings |
| Notifications | Push (FCM) and in-app notification list |
| Profile | Manage the user profile |

## Architecture

```
lib/
├── core/        # API service (Dio + interceptors), DI (get_it), theme, helpers
└── features/    # auth, booking, favorite, home, notification, onboarding, payment, profile, rating, search
    └── <feature>/
        ├── data/          # models, data sources, repository implementations
        ├── domain/        # entities, repository contracts
        └── presentation/  # views, Cubits, widgets
```

## Tech stack

Flutter · Dart · flutter_bloc · get_it · Dio · dartz · flutter_stripe · Firebase Messaging ·
flutter_local_notifications · easy_localization · table_calendar · flutter_screenutil · shared_preferences

## Getting started

```bash
flutter pub get
flutter run
```

Requires the Mwaeed REST API, a Firebase project (for notifications) and a Stripe publishable key.

## Author

**Ammar Zeineh**, Flutter Developer · [LinkedIn](https://linkedin.com/in/ammar-zeineh) · [GitHub](https://github.com/AmmarZeineh)
