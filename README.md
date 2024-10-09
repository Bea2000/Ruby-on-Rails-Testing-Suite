# Ruby on Rails Testing Suite

## Overview

This repository contains the tests developed for a Ruby on Rails system created as part of the testing course at Pontificia Universidad Católica de Chile, completed in the second semester of 2022. The system supports two types of users: normal users and administrators, with different sets of permissions. Features include product reviews, purchase requests, wishlist management, product filtering, and even sports court reservations.

## Project Context

The system is an e-commerce platform that allows:

- Normal users to browse, purchase products, send messages, manage wishlists, and book sports courts.
- Admin users to manage all products, messages, and user reviews.
- A humorous twist by integrating JokeAPI for product page entertainment.

## Objectives of the Testing Suite

The primary goal of the testing suite is to ensure the robustness of the platform, covering the following areas:

1. Unit testing of models, controllers, and helpers to verify that each component functions correctly in isolation.
2. Integration testing to confirm that multiple components work together seamlessly, including the user flow for product purchases and wishlist management.
3. System testing (optional, but available) to simulate end-to-end interactions in a real-world scenario.

## Requirements

- Ruby 3.1.3
- Rails 7.x (installed automatically via bundler)
- PostgreSQL

## Setup

1. Set the environment variables DB_USER and DB_PASSWORD in your system for PostgreSQL authentication.

2. Run the following commands to set up the environment:

    ```bash
    bundle install
    rails db:create
    rails db:migrate
    ```

## Running the Application

To start the server locally:

```bash
rails server
```

## Running the Tests

1. Before running the tests, ensure the test database is up to date:

    ```bash
    rails db:migrate RAILS_ENV=test
    ```

2. To execute the MiniTest unit and integration tests:

    ```bash
    rails test
    ```

3. To run the RSpec tests:

    ```bash
    rspec
    ```

## Testing Focus

The tests focus on critical functionalities such as:

- **Product and stock management**: Ensuring the correct stock is updated when a product is purchased or returned.
- **User roles and permissions**: Verifying that normal users and admin users have access only to the appropriate sections of the platform.
- **Purchase requests**: Testing the process of sending, accepting, or rejecting purchase requests, and ensuring stock is properly adjusted.
Messaging system: Ensuring that users can communicate with sellers through a message system.

## Admin Account Creation

To create an admin account for testing, you can create a user via the registration form and use the keyword admin as the secret password. This is a temporary setup for ease of testing.