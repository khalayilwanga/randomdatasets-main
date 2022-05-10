# Randomdatasets- Full stack developer assessment task

The task is to create a frontend that shows a graph.

1. Frontend must use ReactJS, Flux or Redux, ChartJS for graphing and bootstrap.
2. Backend must use Python, Flask, MySQL and Alembic.

You must create a docker file or a docker-compose script to run both the frontend and the backend.

## Frontend

Have a ChartJS graph that takes up 1/3 the screen width and under half the screen height

The initial set of data comes from the backend, the data can be just simply 5 random dollar values associated with dates starting from Oct 10

For example
$1,000 Oct 10, $2,000 Oct 11 $3,000 Oct 12 $2,500 Oct 13, $4,000 Oct 14

There are also two buttons called create and delete.

Create sends a request to the server to create a new dataset filled with random values but for the same dates.

Once the data is created, the front end should create a new graph which takes up 1/3 the screen. Once you have 4 graphs, the 4th graph should be shown on a new line

Delete deletes the LAST displayed dataset on the screen.

If I refresh the page, then I should get the latest dataset (i.e. the data should be fetched from the backend).
Flux or Redux should be used for sending events to call the backend and when the data is received too.

## Back end

Backend must be a Flask server. The data of the graphs must be stored in a MySQL database. You must use Alembic to check if the right tables were created and create them if necessary.

## Docker

You must create a docker file or a docker-compose script to run both the frontend and the backend separately.

--------------------------------------------------------------------------------------------------------------------------------------
## Solution

Find the docker-compose script to run all 3 containers within the same network at the root of this repository.

To run all containers:  
`docker-compose --env-file sample.env up`  
To stop all containers:  
`docker-compose --env-file sample.env down`

Repositories relevant to the project:  
frontend:found [here](https://github.com/khalayilwanga/randomdatasets-frontend)  
backend:found [here](https://github.com/khalayilwanga/randomdatasets-backend)
