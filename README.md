## Stargate NodeJS Example

The Stargate NodeJS Example is a project that exercises Stargate's schemaless API on Astra. The
use case is storing game state for a game called BattleStax in a single document. The usage 
examples live in the `stargate.test.js` file.

### Prerequisites
-  NodeJS 12+
-  (Recommended) Setup your local development environment with [nodeenv](#nodeenv)

### Using `nodeenv`

Using [nodeenv](https://github.com/ekalinin/nodeenv) allows you to keep your NodeJS version and dependencies isolated for the project you're 
working on. To get started using it for Stargate NodeJS Example, install it using [homebrew](https://formulae.brew.sh/formula/nodeenv) or `easy_install`.
```sh
# install using homebrew
brew install nodeenv

# install using easy_install
sudo easy_install nodeenv
```

Once nodeenv is installed, setup a virtualenv in the project root folder, and then activate it.
```sh
# setup a nodeenv in the venv folder using NodeJS 12
nodeenv venv --node=12.18.3

# activate the nodeenv
. venv/bin/activate

# install dependencies
npm install
```

### Running the Stargate NodeJS Example

Make sure the package dependencies are installed (you should be using nodeenv as described above)
```sh
# install dependencies
npm install
```

Then, create a `.env` file in the project root that is copied from `.env-template`. Add in your Astra specific credentials.

Once your `.env` file is setup, you can run the tests to try out Stargate
```sh
# run the unit tests
npm test
```

### Using the example

You can add additional files or use the `stargate.js` file in your own app as a simple client.

### Postman

A postman collection is included in `postman.json`. To add it to Postman, simply import it, then edit the collection to add 
your Astra specific variables and an auth token. You can download postman here: 
[https://www.postman.com/downloads/](https://www.postman.com/downloads/)
