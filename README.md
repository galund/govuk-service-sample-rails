This is a sample app that includes the [GOV.UK Design System](https://design-system.service.gov.uk/).

It was created as follows:

1. Create a [`Dockerfile`](./rails-app/Dockerfile) for the app server.

2. Create a [`docker-compose.yml`](./docker-compose.yml) to create a minimal development
   environment. Build the environment:

   ```
   docker-compose build
   ```

3. Create the basic rails application:

   ```
   docker-compose run app rails new . --force --no-deps --database=postgresql
   ```

4. Modify the [database config](rails-app/config/database.yml) to point to the DB in our development environment.

5. Update [`package.json`](rails-app/package.json) to include a link to the Design system, and update
   [`rails-app/app/assets/stylesheets/application.css`](rails-app/app/assets/stylesheets/application.css)
   to load up the GOV.UK Design System CSS.

