### Continious integration
We're using Travis for our non-private code such as [payment infrastructure](https://github.com/enhancv/mongoose-subscriptions) and Codeship for our core product as their servers are a lot more powerful. We also implemented a system, that allows us to create a staging version of each branch just by opening a pull request on `Github`. A link to it is posted in `Slack` when its ready. Even though our server and client code is tested with `unit` and `integration` tests, our [deployment process takes less than 5 minutes to complete](https://viktorkirilov.me/post/how-we-sped-up-builds-by-parallelizing-tasks/) thanks to heavy parallelization.

### Infrastructure
- All of our public static files are cached in `AWS Cloudfront`.
- Our main HTTP API is hosted on `Heroku`
- Workers, such as content improvement AI, image resizers, PDF generators are deployed to `AWS Lambda` with `AWS ApiGateway`, which allow us to scale indefinitely.
- User files such as user avatars are deployed directly from the client to `AWS S3` and then processed by a Lambda without going through our servers.
- All our logs are collected in `AWS Cloudfront` and we're able to monitor all of our resources via single dashboard.

### Technologies
- Latest ES6 features + React + Redux + Webpack
- NodeJS for API/Workers
- Python for Content Improvement / AI
- MongoDB as primary database, Postgres for product analytics
- PhantomJS for PDF rendering
- WebDriverIO for integration tests
- Mocha/Chai for unit tests
- Serverless for `AWS Lambda` infrastructure management

### Tools
- `Github` - Open source and private projects (your private contributions will be visible in your github profile)
- `Kanbanize` - Project management
- `Codeship` - Continuous Integration
- `Travis` - Continuous Integration for open source projects
- `Invision` - Wireframes / Prototypes / Product designs
- `Google Drive` - File sharing
- `CodeClimate` - Code coverage
- `Slack` - For team communication
