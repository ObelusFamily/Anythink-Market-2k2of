# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including
all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file
([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull
request against `main` from a feature/bug branch and add `@vanessa-cooper` as
reviewer.

## Setup

### Running the app

```shell
docker-compose up
```

After a while (some pulls and installations) you should see the following
message:

```text
anythink-frontend  | Compiled successfully!
anythink-frontend  |                                                                           
anythink-frontend  | You can now view anythink-market-front in the browser.
```

To test the backend, run the following command:

```shell
if [ $(curl -X GET "http://0.0.0.0:3000/api/ping" | jq ". | length") = 0 ]; then echo "Backend works"; fi
```

### Creating the first user

Go to http://localhost:3001/register and create a new user.
