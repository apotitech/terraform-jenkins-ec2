pipeline {
    agent any
    tools {
       terraform 'terraform'
    }
    stages {
        stage('Git checkout') {
           steps{
                url: 'https://github.com/apotitech/terraform-jenkins-ec2'
            }
        }
        stage('terraform format check') {
            steps{
                sh 'terraform fmt'
            }
        }
        stage('terraform Init') {
            steps{
                sh 'terraform init'
            }
        }
        stage('terraform apply') {
            steps{
                sh 'terraform apply --auto-approve'
            }
        }
    }

    
}
