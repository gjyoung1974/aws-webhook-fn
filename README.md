# Generic WebHook listener Lambda Function for AWS     

## Usage

```
$ npm install -g serverless
$ serverless install --url https://github.com/alexdebrie/webhook-to-cloudtrail --name my-flask-app
$ cd my-flask-app && npm run setup
<answer prompts>
$ serverless deploy
```

Once the deploy is complete, run `sls info` to get the endpoint:

```sh
$ sls info
Service Information
<snip>
endpoints:
  ANY - https://abc6defghi.execute-api.us-east-1.amazonaws.com/dev <-- Endpoint
  ANY - https://abc6defghi.execute-api.us-east-1.amazonaws.com/dev/{proxy+}
```

#### Invoke via curl:     

````sh
curl --header "Content-Type: application/json" --request POST --data '{"something":"xyz","somethingelse":"xyz"}' http://127.0.0.1:5000
````

