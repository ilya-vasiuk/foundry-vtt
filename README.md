### Fly.io deployment config for [Foundry VTT](https://foundryvtt.com)

1. Install [flyctl](https://fly.io/docs/flyctl/)
2. Execute ``flyctl launch`` and remember app name
3. Create volume with ``flyctl volumes create`` and remember volume name
4. Use ``flyctl secrets set FOUNDRY_USERNAME="" FOUNDRY_PASSWORD="" FOUNDRY_ADMIN_KEY=""`` to add your credentials as env parameters
5. Rewrite config with ``cp fly.toml.dummy fly.toml`` and fill app and volume names
6. Deploy your app with  ``flyctl deploy``

If you want to use S3 as static assets storage, than check guide [here](https://foundryvtt.com/article/aws-s3/)

1. Copy aws config with ``cp awsConfig.json.dummy awsConfig.json`` and fill in credentials
2. Uncomment FOUNDRY_AWS_CONFIG line in fly.toml
3. Redeploy your app with ``flyctl deploy``