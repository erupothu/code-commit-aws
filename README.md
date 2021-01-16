# code-commit-aws

## Below are the steps to code commit

1. create IAM user: https://console.aws.amazon.com/iam/home#/home
  a. add user -> username, aws console access -> next -> add permisions -> AWSCodeCommitFullAccess, AWSCodeCommitPowerUser -> add
  b. go to created user -> security -> generate credentials -> copy username, password
  
2. create code commit repository: https://ap-south-1.console.aws.amazon.com/codesuite/codecommit/repositories?region=ap-south-1
  a. repositories -> created repository -> name, description -> create
  b. go to repositoryies -> select repository you want -> copy https clone
  
3. open any ide (eclipse or vs ide):
  a. create project -> right click on project -> Team -> share -> select git -> url: paste selected https clone repo, paste IAM username and password -> next finish
  
4. make any changes in project and commit changes to repository done.

5. changes are updated in code commit repository.
