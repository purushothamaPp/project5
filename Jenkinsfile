pipeline{
    agent any
    stages{
       stage('git checkout'){
          steps{
            checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'git_cred', url: 'https://github.com/purushothamaPp/cicd-project-2.git']])
            
          }
       
       }
        stage('build'){
            steps{
              sh "mvn clean package"
          }
       }
        stage('docker build'){
            steps{
              sh "docker build . -f purushothamareddy/project1  "
            }
        }
        
    
    }
}
