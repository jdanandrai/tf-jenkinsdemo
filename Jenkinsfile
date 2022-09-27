pipeline {
    agent{
        any
    }
    stages{
        stage("inittilize terraform"){
            steps{
                sh "terraform init"
            }
        }
        stage("checking terraform plan"){
            steps{
                sh "terraform plan --auto-approve"
            }
        }
        stage("format terraform file"){
            steps{
                sh "terraform fmt"
            }
        }
        stage("apply"){
            steps{
                sh "terraform apply --auto-approve"
            }
        }
    }
}

