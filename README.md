# Christmas Docker Task in FastAPI

This FastAPI project is a simple Elf Delivery System that allows you to manage packages and elves efficiently.

## Getting Started

### Prerequisites
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

### Running the Application

1. Clone the repository:

    ```bash
    git clone <https://github.com/Sequin13/Christmas-Docker-Task-from-Specialized-Tool-Software.git>
    cd <repository-directory>
    ```

2. Build and run the Docker container:

    ```bash
    docker-compose up --build
    ```

   This will build the Docker image, install dependencies, and start the FastAPI application on port 8000.

3. Access the API:

   Open your browser and go to [http://localhost:8000/docs](http://localhost:8000/docs) to view the FastAPI Swagger documentation. 

## API Endpoints

### Packages

#### Add a Package
- **Endpoint**: `POST /package`
- **Parameters**:
  - `name` (string): Name of the package
  - `elfID` (integer): ID of the elf responsible for the package

#### Update Package Status
- **Endpoint**: `PUT /package`
- **Parameters**:
  - `pack_id` (integer): ID of the package to update
  - `status` (boolean): New status of the package

#### Get Package by ID
- **Endpoint**: `GET /package`
- **Parameters**:
  - `pack_id` (integer): ID of the package to retrieve

#### Delete Delivered Packages
- **Endpoint**: `DELETE /package`

### Elves

#### Add an Elf
- **Endpoint**: `POST /elfs`
- **Parameters**:
  - `elf_name` (string): Name of the elf

#### Update Elf Information
- **Endpoint**: `PUT /elfs`
- **Parameters**:
  - `elfID` (integer): ID of the elf to update
  - `vacation` (boolean): Elf's vacation status
  - `daternity` (boolean): Elf's paternity leave status

#### Get Elf by ID
- **Endpoint**: `GET /elfs`
- **Parameters**:
  - `elfID` (integer): ID of the elf to retrieve

#### Delete Elf
- **Endpoint**: `DELETE /elfs`
- **Parameters**:
  - `elfID` (integer): ID of the elf to remove

## Stopping the Application

To stop the application, press `Ctrl + C` in the terminal where the Docker container is running.

