# Chat with Laravel Reverb

## Overview
This is a simple application created as part of my exploration into Laravel Reverb, specifically aimed at understanding the capabilities of real-time event broadcasting. It provides foundational code for a chat system where users can interact within a private channel, sending and receiving messages instantly. This project served as my starting point to learn and implement real-time communication functionalities using Reverb.

## Features
- **User Authentication**: Includes basic Laravel authentication to manage user access and registration.
- **Real-Time Messaging**: Users can send and receive messages instantly without needing to refresh their browser.
- **Presence Channels**: Utilize Laravel Echo's presence channels to see who is online and available for messaging.
- **Scalable Architecture**: Built to be scalable with Laravel's powerful services, making it suitable for expanding into more complex applications.

### Documentation Links
- [Laravel Reverb Documentation](https://laravel.com/docs/11.x/reverb)
- [Pusher Channels Documentation](https://laravel.com/docs/11.x/broadcasting#client-pusher-channels)
- [ShouldBroadcast Interface Documentation](https://laravel.com/docs/11.x/broadcasting#the-shouldbroadcast-interface)
- [Listening for Event Broadcasts Documentation](https://laravel.com/docs/11.x/broadcasting#listening-for-event-broadcasts)

## Tech Stack
Laravel Version 11.2.0

## Getting Started
This guide provides a structured and detailed guide for setting up and running the simple Chat Laravel Reverb project. It includes prerequisites, a step-by-step installation guide, and links for accessing the application and its documentation.

## Prerequisites
Before you begin, ensure you have the following installed:
- Docker
- PHP >= 8.2
- Composer
- Node.js

### Installation Guide
Follow these steps to set up the "laravel-reverb-chat" project on your local machine:

#### 0. Clone the project:
Open a terminal in your desired directory and clone the repository:
```bash
git clone https://github.com/bertogross/laravel-reverb-chat.git
```
Once cloned:
```bash
cd laravel-reverb-chat
```

#### 1. Install Project Dependencies:
Navigate to the project's root directory and install the required PHP and JavaScript dependencies:
```bash
composer install
```
```bash
npm install
```

#### 2. Generate a new application key:
```bash
php artisan key:generate
```

#### 3. Start Docker Containers (in a new terminal):
Ensure Docker is installed and running on your system. Then, initialize the Docker containers:
```bash
docker-compose up --build
```

#### 4. Set Up and Seed the Database:
Set up the database schema with Laravel's migration feature. By default, the password for all seeded user accounts is set to 'password'.
```bash 
php artisan migrate:fresh --seed
```

#### 5. Compile Frontend Assets (in a new terminal):
Compile the frontend assets using Laravel Mix:
```bash 
npm run dev
```

#### 6. Start the Laravel Development Server (in a new terminal):
```bash 
php artisan serve
```

#### 7. Start the Reverb Server (in a new terminal):
```bash 
php artisan reverb:start --host=127.0.0.1 --port=9000
```

## Accessing the Application
#### Application: http://localhost:8000
#### phpMyAdmin: http://localhost:8080


### Contribute
Please feel free to fork the repository!
