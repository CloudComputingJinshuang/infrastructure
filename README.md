# infrastructure
1. clone files into local folder
2. install AWS CLI flowing the link https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html
3. crete two profiles for demo and dev account 
4. configure local environment for example:
   ~ export AWS_REGION=us-east-1
   ~ export AWS_PROFILE=dev 
5. run cmd in the same directory with csye6225-infra.yml
   aws cloudformation create-stack --stack-name myVPC --template-body file://csye6225-infra.yml --parameters ParameterKey=EnvironmentName,ParameterValue=envForMyVPC
6. check if stack has been created successfully
7. delete stack using below cmd:
   aws cloudformation delete-stack \
    --stack-name myVPC