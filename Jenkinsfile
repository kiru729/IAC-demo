pipeline {
    agent any
    tools {
        terraform 'terraform-1.1.6'
    }
    stages{
        stage('git checkout'){
            steps{
                git credentialsId: 'github-kiru', url: 'https://github.com/kiru729/IAC-demo'
            }
        }
        stage('terraform init'){
            steps{
                sh 'terraform init'
            }
        }
        stage('terraform apply'){
            steps{
                sh 'terraform apply --auto-approve'
            }
        }
    }

}
