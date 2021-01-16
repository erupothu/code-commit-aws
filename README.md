# code-commit-aws

## Below are the steps to code commit

1. create IAM user: https://console.aws.amazon.com/iam/home#/home \
  a. add user -> username, aws console access -> next -> add permisions -> AWSCodeCommitFullAccess, AWSCodeCommitPowerUser -> add \
  b. go to created user -> security -> generate credentials -> copy username, password \
  
2. create code commit repository: https://ap-south-1.console.aws.amazon.com/codesuite/codecommit/repositories?region=ap-south-1 \
  a. repositories -> created repository -> name, description -> create \
  b. go to repositoryies -> select repository you want -> copy https clone \
  
3. open any ide (eclipse or vs ide): \
  a. create project -> right click on project -> Team -> share -> select git -> url: paste selected https clone repo, paste IAM username and password -> next finish \
  
4. make any changes in project and commit changes to repository done. \

5. changes are updated in code commit repository. \

6. Download code commit code to EC2 instance: https://ap-south-1.console.aws.amazon.com/ec2/v2/home?region=ap-south-1#Instances:instanceState=running \
  a. create ec2 micro instance with 20GB, generate pem key and download \
  b. go to local machine -> open terminal -> ssh -i generated_key.pem ubuntu@public_ip \
  c. after successfull login -> create workspace, mkdir workspace, cd workspace -> install git, sudo apt install git \
  d. git clone clone_repo_url \
    1. iam_username: \
    2. iam_password: \
  e. done successfully downloaded the repository to you EC2 server. \
  
7. Deploy java project in EC2 instance or server: \
  a. install java and maven: sudo apt install openjdk-11-jdk maven, java -version, mvn -version \
  b. download package : cd to cloned workspace, cd workspace/cloned_repo, mvn clean install \
  c. java -jar jar_name \
  
8. check from browser: \
  a. http://instance_puclic_ip:port/rest_api \

