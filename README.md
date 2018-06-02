# Agile-Bot

![Agile-Bot](https://uk.legocentric.com/data/lego-0070354-axls-rumble-maker/img/02b7656d-ace2-49bf-9349-8926dcc28d34-small.jpg)

## Development
### First Time Set Up:
Run: `docker-compose run web rails new . --force --database=postgresql`

Now that you’ve got a new Gemfile, you need to build the image again. (This, and changes to the Gemfile or the Dockerfile, should be the only times you’ll need to rebuild.)

`docker-compose build`

You can now boot the app:

`docker-compose up`

Finally, you need to create the database. In another terminal, run:

`docker-compose run web rake db:create`

Go to http://localhost:3000 on a web browser to see the app.

### Day to Day Development (Docker Container):
- To stop the application, run `docker-compose down` in your project directory.
- To restart the application run `docker-compose up`
- If you make changes to the Gemfile or the Compose file to try out some different configurations, you need to rebuild. Some changes require only `docker-compose up --build`

### Instruction that we may want to cover in the future:

* Ruby version
* System dependencies
* Configuration
* Database creation
* Database initialization
* How to run the test suite
* Services (job queues, cache servers, search engines, etc.)
* Deployment instructions
