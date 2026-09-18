# Proposed Solution Architecture

```text
                 ┌──────────────────────────┐
                 │        PASSENGER         │
                 │ Mobile App / Web / Kiosk │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │     NAVIGATION SYSTEM    │
                 │                          │
                 │ • Destination Search     │
                 │ • Station Map            │
                 │ • Route Calculation      │
                 │ • Accessibility Mode     │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │    NAVIGATION ENGINE     │
                 │                          │
                 │   Dijkstra Algorithm     │
                 │   Shortest Path          │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │     STATION DATABASE     │
                 │                          │
                 │ • Platforms              │
                 │ • Restrooms              │
                 │ • Ticket Counters        │
                 │ • Food Courts            │
                 │ • Lifts & Ramps          │
                 │ • Facility Updates       │
                 └──────────────────────────┘

        ┌─────────────────────────────────────┐
        │          ADMIN DASHBOARD            │
        │ Update facilities & station layout  │
        └─────────────────────────────────────┘                                                                                      Working
Passenger opens the application or kiosk.
Passenger selects a destination.
The system identifies the starting point.
The navigation engine calculates a suitable route.
The route is displayed on the station map.
Voice guidance provides directions when enabled.
Administrators can update station information.
