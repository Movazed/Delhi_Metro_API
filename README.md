# Delhi Metro API

Welcome to the Delhi Metro API! This API provides information about the Delhi Metro routes, stations, fare details, and other related data. The aim is to make it easier for developers to build applications and services that utilize Delhi Metro information.

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [API Endpoints](#api-endpoints)
    - [Get All Stations](#get-all-stations)
    - [Get Route Between Stations](#get-route-between-stations)
    - [Get Fare Details](#get-fare-details)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

### Prerequisites

Before you begin, ensure you have met the following requirements:
- You have Node.js and npm installed on your machine.

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/your-username/delhi-metro-api.git
    ```

2. Change to the project directory:

    ```sh
    cd delhi-metro-api
    ```

3. Install the required packages:

    ```sh
    npm install
    ```

4. Start the server:

    ```sh
    npm start
    ```

## Usage

### API Endpoints

#### Get All Stations

- **Endpoint**: `/api/stations`
- **Method**: `GET`
- **Description**: Retrieves a list of all metro stations.
- **Response Example**:

    ```json
    [
      {
        "id": 1,
        "name": "Rajiv Chowk",
        "line": "Blue Line"
      },
      {
        "id": 2,
        "name": "Kashmere Gate",
        "line": "Red Line"
      }
    ]
    ```

#### Get Route Between Stations

- **Endpoint**: `/api/route`
- **Method**: `GET`
- **Parameters**:
  - `from` (string): The starting station name.
  - `to` (string): The destination station name.
- **Description**: Retrieves the route between two stations.
- **Response Example**:

    ```json
    {
      "from": "Rajiv Chowk",
      "to": "Kashmere Gate",
      "route": [
        "Rajiv Chowk",
        "New Delhi",
        "Chandni Chowk",
        "Kashmere Gate"
      ],
      "total_time": "20 mins"
    }
    ```

#### Get Fare Details

- **Endpoint**: `/api/fare`
- **Method**: `GET`
- **Parameters**:
  - `from` (string): The starting station name.
  - `to` (string): The destination station name.
- **Description**: Retrieves the fare details between two stations.
- **Response Example**:

    ```json
    {
      "from": "Rajiv Chowk",
      "to": "Kashmere Gate",
      "fare": 30
    }
    ```

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
