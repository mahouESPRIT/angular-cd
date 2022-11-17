
Skip to content
Pull requests
Issues
Codespaces
Marketplace
Explore
@mahouESPRIT
fedi-ba /
cicd_angular
Public

Code
Issues
Pull requests
Actions
Projects
Security

    Insights

cicd_angular/Jenkinsfile
@fedi-ba
fedi-ba Create Jenkinsfile
Latest commit 2e4f214 Nov 10, 2022
History
1 contributor
39 lines (36 sloc) 993 Bytes
pipeline
{
   agent any
    stages {
     stage('Pull') {
      steps{
       script{
     checkout([$class: 'GitSCM', branches: [[name: '*/main']],
         userRemoteConfigs: [[
         
         url:'https://github.com/mahouESPRIT/angular-cd']]])
         
         }
      }
     }
    
         }
         }
