# Jaemo

An Android app for booking student pickup and drop-off rides to and from school, with interactive map-based location selection. Built as a university Final Year Project.

## Overview

Jaemo lets a parent or student book a ride by picking a pickup and drop-off point on a map, setting the school's start/end times, and choosing a one-way or two-way trip. After entering student/customer details, the app matches and books a driver for the route. Maps are rendered with OpenStreetMap data via osmdroid, including offline vector tiles (Mapsforge), WMS layers, and GeoPackage support.

## Features

- **Map-based pickup/drop-off selection** — interactive OSM map for choosing locations
- **Trip configuration** — one-way or two-way, with school start/end times
- **Student/customer details form** — name, age, gender captured per booking
- **Route booking & driver matching** — "Book Route" and "Find Driver" flow
- **Offline & alternate map sources** — Mapsforge (offline vector maps), WMS, and GeoPackage support via osmdroid

## Tech Stack

Java, Android SDK (Gradle), osmdroid (OpenStreetMap, WMS, Mapsforge, GeoPackage), Android Navigation Component, Material Components, AndroidX

## Project Structure

```
FYP/
└── app/
    └── src/main/java/com/jaemo/jaemo/
        ├── MainActivity.java
        └── customer/
            ├── dropoff/DropoffActivity.java
            ├── customer_info/CustomerInfoActivity.java
            └── book_route/BookRouteActivity.java
```

## Getting Started

1. Clone the repo and open it in Android Studio.
2. Let Gradle sync (min SDK 15, target SDK 29).
3. Run on an emulator or device — location permissions are required for map and pickup/drop-off features.

## Permissions

`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`, `INTERNET`, `ACCESS_NETWORK_STATE`, `READ/WRITE_EXTERNAL_STORAGE` — used for live location, map tile loading, and offline map caching.

## License

MIT
