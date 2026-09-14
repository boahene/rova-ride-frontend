# Rova Ride-Hailing Frontend

Rova is an Accra-focused ride-hailing frontend prototype with a Rider Guest and Driver Guest simulation flow.

## Run the simulation

Open `rideflow-frontend.html` in a browser. For the two-account flow:

1. Open the file in two browser windows on the same browser origin.
2. Choose **Rider Guest** in one window.
3. Choose **Driver Guest** in the other.
4. Request the Driver Guest from the rider window.
5. Accept and complete the trip from the driver window.

The current browser demo uses `BroadcastChannel` with a `localStorage` fallback. Replace this event layer with WebSockets or another realtime service when the backend is added.

## Product rules represented in the UI

- Accra, Ghana launch context with Ghana phone sign-in.
- Nearby available drivers and drivers finishing nearby.
- Direct driver requests by full name or number plate.
- Three-minute free cancellation window after driver matching.
- ₵5 chargeable cancellation fee: ₵3 to the affected driver and ₵2 to Rova.
- Five free pickup-waiting minutes, then ₵0.10 per chargeable minute.
- A 30% Rova platform fee on the ride fare only; waiting-time charges go fully to the driver.
- Rider and driver bill views at trip completion.

## Backend seams

The prototype keeps authentication, driver matching, location updates, chat, calling, billing, cancellation settlement, and persistence as frontend placeholders for later implementation.