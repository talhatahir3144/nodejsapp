pipeline{
    agent any
    tools{
        nodejs 'nodejsjenkins'
    }
    stages{
        /*stage('Testing-Node'){
            steps{
                sh "npm version"
            }
        }
        stage('pull-data-from-git'){
            steps{
                git credentialsId: 'GitHubCreds', url: 'https://github.com/mtalhatahir/nodejsapp.git'
            }
        }
        stage('Building-App'){
            steps{
                sh "npm install package.json"
            }
        }*/
        stage(deploy){
            steps{
            sshagent(['admin1']) {
                sh '''ssh -tt - StrictHostKeyChecking=no admin1@192.168.117.128 "ls -al" 
                
                '''
                }
            }
        }
        /*stage('Run-App'){
            steps{
                sh "npm start"
            }
        }*/
    }

}