# Blockchain Project with Rust and Actix Web

Welcome to the Blockchain Project! This project demonstrates the implementation of a simple blockchain using Rust and the Actix Web framework. It includes the core components of a blockchain, such as blocks, transactions, mining, and chain validation. The project also features a web server to interact with the blockchain through HTTP requests.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Testing with Postman](#testing-with-postman)
- [License](#license)

## Introduction
This project serves as a basic introduction to blockchain technology and Rust programming. It implements a blockchain with essential functionalities like creating transactions, adding blocks, mining, and validating the chain. The project also includes a web server built with Actix Web to provide a REST API for interacting with the blockchain.

## Features
- **Blockchain Implementation**: Core features including blocks, transactions, and mining.
- **Web Server**: Actix Web server for interacting with the blockchain via HTTP requests.
- **Chain Validation**: Ensures the integrity of the blockchain.
- **Persistence**: Load and save the blockchain to a file.

## Requirements
- Rust (latest stable version)
- Cargo (Rust package manager)
- Postman (for testing the API)

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/SuryodayDevHub/blockchain_challenge.git
   cd blockchain_challenge
2. **Install dependencies**:
   ```bash
   cargo build
3. **Run the application**:
   ```bash
   cargo run

## Usage
After running the application, the server will start on `http://127.0.0.1:8080`. You can interact with the blockchain via the provided endpoints.

## Endpoints
- **GET /chain**: Retrieve the entire blockchain.
  - **Response**: JSON representation of the blockchain.

- **POST /add_block**: Add a new block with transactions.
  - **Request Body**: JSON array of transactions, each containing `sender`, `receiver`, and `amount`.
  - **Response**: Confirmation message.

## Testing with Postman
- **Get the Blockchain**:
  - **Method**: GET
  - **URL**: `http://127.0.0.1:8080/chain`
  - **Response**: JSON of the current blockchain.

- **Add a Block**:
  - **Method**: POST
  - **URL**: `http://127.0.0.1:8080/add_block`
  - **Body** (raw JSON):
    ```json
    [
      {
        "sender": "Alice",
        "receiver": "Bob",
        "amount": 50.0
      },
      {
        "sender": "Bob",
        "receiver": "Charlie",
        "amount": 25.0
      }
    ]
    ```
  - **Response**: JSON confirmation message.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
