# What is this
This is an example of serverless-framework setup which sets up Cognito user pool and two routes:
* publicly available route
* route under authorizer

# How to deploy
1. Do `npm install` within `./layers/nodejs` directory
2. Edit `serverless.yml` for empty values
* callbackuri: #POPULATE ME
* pool-domain: #POPULATE ME
3. Return to project root and do `serverless deploy`

# After deployment
One route will be immediately available, for the other one you will need to provide bearer token in the request under Authorization header (specified by `IdentitySource` key in `serverless.yml`).
You need to create a cognito user and use "Hosted UI" to login and get id_token. Once you have it use it as value for Authorization header.

# Disclaimer
This code only servers as learning example to understand how to setup Cognito authorization and to protect your API route. It should not be used as a production code since this serves as minimal setup required to achieve desired.