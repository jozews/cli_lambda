# Lambda

Command Line Interface for AWS Lambda built on top of [boto3](http://boto3.readthedocs.io/en/latest/reference/services/lambda.html).

## Set up

Set up environmental variables:
LAMBDA_PATH: a directory where your function will live locally
AWS_ACCESS_KEY_ID: access key to your AWS account
AWS_SECRET_ACCESS_KEY: secret key to your AWS account
AWS_DEFAULT_REGION: the default region of your lambda functions
ROLE: IAM Role assigned to your functions

## Basic Usage

Create a new function
`lambda my_function create`

Update function code
`lambda my_function update_code`

Invoke function with specified event
`lambda my_function invoke --event '{"event_key" : "event_value"}'`

## All available commands
`create`
Optional parameters: --runtime --description --timeout --publish

`create_alias`
Required paramateres: --alias --version
Optional parameters: --description

`delete`
Required paramateres: --qualifier

`get`
Optional paramateres: --qualifier

`get_aliases`
None

`get_configuration`
None

`invoke`
Optional paramateres: --event

`invoke_local`
Optional paramateres: --event

`update_alias`
Required paramateres: --alias

`update_code`
Optional paramateres: --publish

`update_configuration`
Optional paramateres: --role --runtime --description --timeout
