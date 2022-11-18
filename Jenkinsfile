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
     stage ('build'){
      steps{
        script{
            sh  "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml"
        }  
      }
     
     }
      stage('docker'){
            steps{
                script{
                    sh "ansible-playbook Ansible/docker.yml -i Ansible/inventory/host.yml "
                }
            }
        }
      stage('docker-registry'){
            steps{
                script{
                    sh "ansible-playbook Ansible/docker-registry.yml -i Ansible/inventory/host.yml"
                }
            }
        }
     
         }
         }
