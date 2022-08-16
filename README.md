# Solita's Dev Academy Assignment

![App Image Preview](https://github.com/hgabs/solita-devacademy-assignment/raw/master/app.png)

The application consists of three parts:

- PostgreSQL Database
- Express.js API back end
- React.js front end

## Deployment

To deploy the application locally using docker containers, you will need to have **docker-compose** installed. Execute the commands below from the main repository directory.

#### 1. Clone the Repository and its Submodule

>git clone --recurse-submodules https://github.com/hgabs/solita-devacademy-assignment.git

#### 1. Download CSV files

Download the follwing CSV files to the data folder in the backend repository.
* <https://dev.hsl.fi/citybikes/od-trips-2021/2021-05.csv>
* <https://dev.hsl.fi/citybikes/od-trips-2021/2021-06.csv>
* <https://dev.hsl.fi/citybikes/od-trips-2021/2021-07.csv>

>curl -L -O https://dev.hsl.fi/citybikes/od-trips-2021/2021-05.csv -O https://dev.hsl.fi/citybikes/od-trips-2021/2021-06.csv -O https://dev.hsl.fi/citybikes/od-trips-2021/2021-07.csv

#### 2. Build Images

>docker-compose build

#### 3. Start Containers

>docker-compose up -d

#### 4. Parse and Save CSV Data to Database

>docker exec -it \<api-container-name\> npm run csv:import

If there are no conflicts with the required ports, you should be able to view the frontend by visiting http://localhost:3000
