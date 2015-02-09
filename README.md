# Acme Air in NodeJS 

## Content

### Datasource Choices

* MongoDB 
* Cloudant

Use environment virable dbtype=mongo or dbtype=cloudant to determine which data type to use. 
It is automactially discovered when running on Bluemix from the service the application is bound to.

### Application Flovors

* Monolithic 
* Micro-Service

Use authService=host name:port to point to the autentication micro-service.


## How to get started

### Resolve module dependencies

	npm install

### Run Monolithic on Local

	node app.js
		
### Run Micro-Service on Local

	node authservice-app.js
	set authService=localhost:9443
	node app.js
	
### Access Application 

	http://localhost:9080/
	Load Database 
		preload 10k customers uid[0..9999]@email.com:password, 5 days' flights.  Defined in loader/loader-settings.json
	Login
	Flights
		such as Singapore to HongKong or Paris to Moscow 
	Checkin
		cancel some booked flights
	Account
		update account info
	Logout	
	
## Run on Other Platform

* [BLuemix] (README_Bluemix.md)
* [Bluemix Container Service] (README_Bluemix_Container.md)
* [Docker] (README_Docker.md)
