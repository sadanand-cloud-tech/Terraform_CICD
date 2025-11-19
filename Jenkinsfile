pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
              git branch: 'main', url: 'https://github.com/sadanand-cloud-tech/Terraform_CICD.git'
            }
        }
        stage('init') {
            steps {
               sh 'terraform init'
            }
        }
        stage('plan') {
            steps {
              sh 'terraform plan'
            }
        }
        stage('apply') {
            steps {
              sh 'terraform apply -auto-approve'
            }
        }
    }
}
