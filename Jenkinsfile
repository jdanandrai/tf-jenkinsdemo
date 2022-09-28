pipeline {
    
    agent{
        label "${label}"
    }
    
    stages{
        stage("inittilize terraform"){
            steps{
                sh "terraform init"
            }
        }
        stage("checking terraform plan"){
            steps{
                sh "terraform plan"
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

