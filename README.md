# QdQ

QdQ is a mobile-first virtual queue management application that helps users avoid standing in physical queues.

Users can:
- create queues
- join queues using QR codes
- track queue position
- leave queues
- automatically promote the next person as queue head

The application is built using:
- Ionic + Angular
- .NET 8 Web API
- Entity Framework Core
- SQL Server
- Azure App Service

---

# Features

## Authentication
- Phone number login
- OTP verification
- JWT authentication
- First-time profile setup
- Passwordless authentication

---

## Queue Management
- Create queue
- Join queue
- Leave queue
- Automatic head promotion
- Token number generation
- Queue member tracking

---

## QR Features
- Generate queue QR code
- Scan QR code
- Join queue via QR

---

## Queue View
Users can view:
- Current queue head
- Token number
- People ahead
- Queue members

---

## Head Controls
Queue head can:
- Exit queue
- Automatically promote next person as head

Members can:
- Leave queue anytime

---

# Tech Stack

| Layer | Technology |
|-------|-------------|
| Frontend | Ionic Framework + Angular |
| Backend | .NET 8 Web API |
| ORM | Entity Framework Core |
| Database | SQL Server |
| Hosting | Azure App Service |
| Authentication | JWT + OTP |
| OTP Service | Twilio / MSG91 |

---

# System Architecture

```text
+------------------------------------------------------+
|                  MOBILE APPLICATION                  |
|------------------------------------------------------|
| Ionic + Angular + Capacitor                          |
|                                                      |
| Features:                                            |
| - Login with OTP                                     |
| - Create Queue                                       |
| - Scan QR                                            |
| - Join Queue                                         |
| - Leave Queue                                        |
| - View Queue Status                                  |
| - Head Controls                                      |
+------------------------------------------------------+
                    |
                    |
                    | HTTPS REST APIs
                    |
                    v
+------------------------------------------------------+
|                ASP.NET CORE WEB API                  |
|------------------------------------------------------|
| Modules:                                             |
| - Authentication                                     |
| - Queue Management                                   |
| - QR Management                                      |
|                                                      |
| Responsibilities:                                    |
| - OTP Verification                                   |
| - JWT Authentication                                 |
| - Queue Creation                                     |
| - Queue Join                                         |
| - Queue Exit                                         |
| - Head Promotion                                     |
| - Token Assignment                                   |
| - QR Validation                                      |
+------------------------------------------------------+
                    |
                    |
                    v
+------------------------------------------------------+
|                  SQL SERVER DATABASE                 |
+------------------------------------------------------+
| Tables:                                              |
| - Users                                              |
| - OtpVerifications                                   |
| - Queues                                             |
| - QueueMembers                                       |
+------------------------------------------------------+

