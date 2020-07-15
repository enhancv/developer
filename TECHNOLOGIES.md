### Continious integration
At Enhancv, we're using Codeship as CI/CD for our products. Deploying to production is as easy as single merge to master and we deploy multiple times per day. Our staging system creates new copy of the app for each branch just by opening a pull request on `Github`. Even though our server and client code is comprehensively tested with `unit` and `integration` tests, our [deployment process takes less than 5 minutes to complete](https://viktorkirilov.me/post/how-we-sped-up-builds-by-parallelizing-tasks/) thanks to heavy parallelization.

### Infrastructure
- Public static files(homepage/enhancv.com/assets in app) are cached in `AWS Cloudfront`.
- Public HTTP API is hosted on `Heroku`
- Workers, such as content improvement AI, image resizers, PDF generators are hosted on `AWS Lambda` with `AWS ApiGateway`.
- User files are deployed directly from the client to `AWS S3`, then processed by a AWS Lambdas.
- `AWS Cloudfront` is used for logging and health-monitoring of our products.

### Technologies
- Latest ES6 features + React + Redux + Webpack
- NodeJS for API/Workers
- Python for Content Improvement / AI
- MongoDB as primary database, Postgres for product analytics
- Headless Chrome for PDF rendering and serverside rendering
- Puppeteer for integration tests
- Mocha/Chai for unit tests
- Serverless for `AWS Lambda` infrastructure management

### Tools
- `Zapier` - We like to automate
- `Github` - Open source and private projects (your private contributions will be visible in your github profile)
- `Airtable` - Project management
- `Codeship` - Continuous Integration
- `Figma` - Wireframes / Prototypes / Product designs
- `Google Drive` - File sharing
- `CodeClimate` - Code coverage
- `Slack` - For team communication
