# Building and Running a Compose File for a Multi-Container Project

> Goal: Create a comose config for a local Drupal CMS website
> Goal: Build and Run Compose file


- Use the `drupal:9.3.13` image along with the `postgres:14.3` image
- 2020 UPDATE: No version nedded in compose files! All 2.x and 3.x features supported without version key.
- Use `ports` to expose Drupal on 8080 (or your preferred port for localhost access)
- Be sure to setup the POSTGRES_PASSWORD environment variable on the postgres service
- Walk through the Drupal config steps in browser at `http://localhost:8080`
- TIP: Drupal setup will assume the database runs on localhost, which is incorrect. You'll need to change it to the name of the service you gave to postgres
- Use Docker Hub documentation to figure out hte right environment and volume settings
- Extra Credit: Use volumes to store Drupal unique data