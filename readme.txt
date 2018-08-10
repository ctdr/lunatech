README

Notes
- airports application available at http://localhost:8000/airports
- countries application available at http://localhost:8000/countries
- health check endpoints available at
    http://localhost:8000/airports/health/live
    http://localhost:8000/airports/health/ready
    http://localhost:8000/countries/health/live
    http://localhost:8000/countries/health/ready


Pre-requisites
-------------------------------------------
1. Docker engine installed

2. Docker compose installed

3. airports-assembly-x.x.x.jar file(s) in airports folder
(naming convention must be exact)

3. countries-assembly-x.x.x.jar file(s) in countries folder
(naming convention must be exact)

4. As per described change for version 1.1.0 of the aiports application
a change needs to made to the nginx default.conf file. This change is 
already in the default.conf file and commented out.


RUN
-------------------------------------------
1. In root directory run
docker-compose up -d --build --remove-orphans

Update to new version of application jar
-------------------------------------------
1. Change environment variable API_VERSION for relevant application dockerfile
(must match version number as appears in jar filename)
2. In root directory run
docker-compose up -d --build --remove-orphans

STOP
-------------------------------------------
1. In root directory run
docker-compose down



