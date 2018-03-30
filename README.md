## lb-connector-firebase

Firebase connector for loopback v3

## Installation of the connector

You’re going to add a MongoDB data source in addition to the MySQL data source created in Connect your API to a data source.

    $ lb datasource

When prompted, respond as follows:

    ? Enter the data-source name: firebase
    ? Select the connector for firebase: Other
    ? Enter the connector's module name: @syncu.be/lb-connector-firebase
    ? Install lb-connector-firebase (Y/n): Y

Add to your datasources.json file the following:

    "firebase": {
        "name": "firebase",
        "url": "https://<% YOUR FIREBASE PROJECT ID %>.firebaseio.com",
        "token": "<% YOUR FIREBASE PROJECT TOKEN %>"
    }

Done!

## Customizing Firebase configuration for tests/examples

The .loopbackrc file is in JSON format, for example:

    {
        "test": {
            "firebase": {
                "url": "<firebase_url>",
                "token": "<security_token>"
            }
        }
    }

## Running tests

 * npm test - To run the test
 * npm run coverage - To find the code coverage

## Release notes
 Yet to be Released officially


## Credits

Inspired by https://github.com/Synerzip/loopback-connector-firebase

Actually, PUT and DELETE queries were not working for our project so we decided to fork Synerzip's connector and maintain it in actual state.