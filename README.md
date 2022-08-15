# Solita's Dev Academy Assignment

The application consists of three parts:

- PostgreSQL Database
- Express.js API back end
- React.js front end

## Deployment

To deploy the application locally using docker containers, you will need to have **docker-compose** installed. Execute the commands below from the main repository directory.

#### 1. Download CSV

Download the follwing CSV files to the data folder in the backend repository.
* <https://dev.hsl.fi/citybikes/od-trips-2021/2021-05.csv>
* <https://dev.hsl.fi/citybikes/od-trips-2021/2021-06.csv>
* <https://dev.hsl.fi/citybikes/od-trips-2021/2021-07.csv>


#### 2. Build Images

>docker-compose build


#### 3. Start Containers

>docker-compose up -d


#### 4. Parse and Save CSV Data to Database

>docker exec -it devacademy-api-1 npm run csv:import

If there are no conflicts with the required ports, you should be able to view the frontend by visiting http://localhost:3000

