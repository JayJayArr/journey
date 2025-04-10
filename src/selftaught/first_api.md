# My First Project

The first project I was ever assigned after teaching myself TS was a small REST-API for a customer.

The task was to run a select-statement with a provided start- and an end-time on the database and return the resulting data.
Looking back it was an awesome task as I had to touch many different subjects I was not yet fully familiar with:

- Implementing basic auth on the API endpoints
- Rate Limiting
- Request headers
- Proper async handling with DB-transactions
- environmental variables
- Database connections (I realized some weeks later that I should not connect to the database every time a request was sent)
- SSL encryption
- SQL prepared statements to protect against SQL injection

I ended up taking aroung two days to set it all up in nestjs and learned a lot because it actually had to run in production.

The plan was to Dockerize the API as soon as it was finished but we settled for PM2 as it was easier to setup on the windows server it was supposed to run on.
Somehow a Dockerfile still ended up in the git repository.
This later led me down a Docker-rabbithole which I am still really grateful for today.

If you want to have a look at the weird code I produced feel free to have a look at it on [Github](https://github.com/JayJayArr/prowatch-custom-api).
