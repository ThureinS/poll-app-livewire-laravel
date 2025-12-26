# Laravel Livewire Poll App

A real-time polling application built with Laravel and Livewire as a learning project. This application allows users to create dynamic polls with multiple options and vote in real-time without page reloads.

## ⚠️ Disclaimer

**This is a learning project.** It is not intended for production using and comes with **no license**. The base framework follows the MIT license, but the application code is for educational purposes only.

## Features ✨

-   **Create Polls**:
    -   Dynamic form to add/remove poll options instantly.
    -   Real-time validation for titles (min 3 chars) and options.
    -   Limit of up to 10 options per poll.
-   **Real-time Voting**:
    -   Users can vote on any option.
    -   Vote counts update instantly across clients using Livewire's reactivity.
    -   Visual progress indication for each option.
-   **Responsive Design**:
    -   Styled with Tailwind CSS (via CDN and Vite).
    -   Mobile-friendly layout.

## Tech Stack 🛠️

-   **Framework**: [Laravel 12](https://laravel.com)
-   **Frontend**: [Livewire 3](https://livewire.laravel.com)
-   **Styling**: [Tailwind CSS](https://tailwindcss.com) (v4 alpha via Vite & CDN)
-   **Database**: MySQL

## Installation 🚀

Follow these steps to set up the project locally:

1.  **Clone the repository** (if you haven't already).

2.  **Install PHP dependencies**:

    ```bash
    composer install
    ```

3.  **Setup Environment**:

    ```bash
    cp .env.example .env
    ```

4.  **Generate Application Key**:

    ```bash
    php artisan key:generate
    ```

5.  **Configure Database**:

    -   **SQLite** (Default): The project is pre-configured for SQLite.
    -   **MySQL**: Update your `.env` file with your MySQL credentials (`DB_CONNECTION=mysql`, `DB_DATABASE`, `DB_USERNAME`, etc.) and ensure the database exists.

6.  **Run Migrations**:

    ```bash
    php artisan migrate
    ```

7.  **Install & Build Assets**:

    ```bash
    npm install
    npm run dev
    ```

8.  **Start the Server**:
    Keep `npm run dev` running in one terminal, and start the Laravel server in another:

    ```bash
    php artisan serve
    ```

9.  **Access the App**:
    Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.

## Usage 💡

1.  **Creating a Poll**:

    -   Enter a "Poll Title".
    -   Add options using the "Add Option" button.
    -   Click "Create Poll".
    -   _Validation rules ensure data integrity (e.g., options cannot be empty)._

2.  **Voting**:
    -   Scroll to the "Available Polls" section.
    -   Click "Vote" on any option.
    -   Watch the vote count increment immediately!

## Security & Code Quality 🔒

-   **Validation**: All user inputs are validated on the server-side using Laravel's robust validation rules (`required`, `min`, `max`).
-   **Mass Assignment Protection**: Eloquent models (`Poll`, `Option`) use `$fillable` to prevent mass assignment vulnerabilities.
-   **Type Safety**: Strictly typed properties and method signatures are used where applicable.

---
