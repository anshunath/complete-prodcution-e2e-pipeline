@Library('jenkins_shared_lib') _
pipeline{

    agent any

    

    stages{
         
        stage('Git Checkout'){
                    
            steps{
            script{
                gitCheckout(
                git branch: 'main', url: 'https://github.com/anshunath/complete-prodcution-e2e-pipeline.git'
                )
            }
            }
        }
        stage('Git Checkout'){
                    
            steps{
            script{
                mvnTest()
            }
            }
        }
        
    }
}