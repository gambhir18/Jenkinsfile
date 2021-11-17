pipeline {
    agent any
    tools{
        terraform "Terraform v1.0.11"
    }

    stages {
        stage('Terraform Init') {
            steps {
                echo 'Initialize Terraform'
                sh 'terraform init'
            }
        }
        stage('Terraform Plan') {
            steps {
                sh 'terraform plan'
            }
        }
        stage('Terraform apply') {
            steps {
                sh 'terraform apply -auto-approve'
            }
        }
    }
}
