pipeline {    
 agent any
    tools { 
        terraform 'terraform-poc-path'
    } 
    stages {
        stage('Git Checkout'){ 
            steps {
                git 'https://github.com/dwdelacruz/iac-demo.git'
            }
        }
        stage('Terraform Init'){
            steps {
                sh 'terraform init'
            }
        }
        stage('Terraform Apply'){
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
