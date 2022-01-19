pipeline {    
 agent any
    options {
      skipDefaultCheckout(true)
    }
    tools { 
        terraform 'terraform-poc-path'
    } 
    stages {
        stage('checkout') {
           steps {
             checkout scm
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
