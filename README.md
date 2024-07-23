# Shopping Basket
A Fullstack App to manage customer's shopping baskets. <br>
Users can register and login to create baskets and check their receipts. <br>
This project was developed using .NET Core 8.0, Angular 16 and PostgreSQL. <br>

## Installing / Getting started
First of all be sure to clone the repository along with the submodules by using the command:
```shell
git clone --recursive https://github.com/AlvesThales/shopping-basket-app.git
```
If you don't use the "--recursive" option the submodules will be empty and the app will fail to run.

To run this application you will need Docker and Docker-compose. Go to the root directory of the app (where docker-compose.yml is) and execute the command:
```shell
docker-compose up -d --build
```

The docker-compose file will do all the job and start the application at the url http://localhost:4200.

The backend may start before the database is running, so it may be necessary to restart it once.

To stop the application just execute the following command:
```shell
docker-compose stop
```

## Technical Overview

Features included:
- Authentication with JWT
- User registration/login/logout
- Form for users to input quantities of each item.
- Creation of baskets with the items available and applying discounts
- Receipt generation including each item, it's price, applied discounts and the total costs with and without discounts
- Fetch product details from a database
- Store baskets to a database and display past transactions
- Unit tests
- Logging
- Code First Migrations
- SOLID design principles
- Design patterns (Strategy, Dependency Injection, etc.)

##  Improvements

Some points to improve if there was more time, or for a real production scenario:
- Increase the Unit Tests coverage to be higher than 80%
- Add integration tests
- Add caching
- Add a monitoring tool such as Kibana
- Parametrize application properties with profiles
- Use vaults to store sensitive data
- Use two databases, one for writing, another for reading