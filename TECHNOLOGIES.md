### Continious integration
We're using Travis for our non-private code such as [payment infrastructure](https://github.com/enhancv/mongoose-subscriptions) or [our homepage](https://github.com/enhancv/homepage) and Codeship for our core product. Our team have always been passionate about improving the development processes, so we implemented a system, that allows us to create a staging version of each branch just by pushing it to `Github` and a link is posted in `Slack`. Even thought our server and client code is tested with `unit` and `integration` tests, our [deployment process takes less than 5 minites to complete](https://viktorkirilov.me/post/how-we-sped-up-builds-by-parallelizing-tasks/).

### Infrastructure
- All of our public static files are catched in `AWS Cloudfront`.
- Our main HTTP API is hosted on `Heroku`
- Workers, such as content improvement AI, image resizers, PDF generators are deployed to `AWS Lambda` with `AWS ApiGateway`, which allow us to scale unlimitedly.
- User files such as user avatars are deployed directly to `AWS S3` without going through our servers and then processed by a Lambda.
- All our logs are collected in `AWS Cloudfront` and we're able to monitor all of our resources via single dashboard.

### Technologies
- Latest ES6 features + React + Redux/Reflux + Webpack
- NodeJS for API/Workers
- Python for Content Improvement / AI
- MongoDB as primary database, Postgres for product analytics
- PhantomJS for PDF rendering
- WebDriverIO for integration tests
- Mocha/Chai for unit tests
- Serverless for `AWS Lambda` infrastructure management

### Tools
- `Github` - open source and private projects(your private contributions will be visible to your github profile)
- `Trello` - Tasks logging
- `Invision` - Wireframes / Prototypes / Product designs
- `Google Drive` - File sharing
- `CodeClimate` - Code coverage
