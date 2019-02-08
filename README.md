# AWS Lambda TEST from Nodejs

Little workaround for the sake to teach myself to use AWS Lambda from Nodejs.
Easy steps:

1. Initialize a nodejs project and install serverless:
```
npm init
npm install -g serverless
```
2. You need a template to create the whole project; to see the available templates you can use: 
```
serverless create --help
```
I will use the nodejs template:
```
serverless create -t aws-nodejs
```
3. Serverless create command creates some boilerplate code for us. We need to edit the serverless.yml file to change parameters of the AWS Service like service name, function details, etc.
4. To deploy it its necesary you get credentials from AWS. For the example I use a Access Key ID from the option Security Credentials. Lets asume the access key is: JULIETAACEVEDO.
5. Now we enter the credentials(the key and the private key) to the serverless framework:
```
serverless config credentials --provider aws --key JULIETAACEVEDO --secret RANDOMSTUFFSECRET
```
6. After this you can deploy your function to aws with the command:
```
serverless deploy
```
This commmand gives you an url where you can get the service.

7. You could use stages with the deploy command:
```
serverless deploy --production
```

That's it! Nothing too fancy or too complicated!