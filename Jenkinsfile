@Library('Jenkins-shared-library') _
pipeline{

    agent any

    

    stages{
         
        stage('Git Checkout'){
                    
            steps{
            script{
                gitCheckout(
                    branch: "main"
                    url: 'https://github.com/anshunath/complete-prodcution-e2e-pipeline.git'
                )
            }
            }
        }
        stage('unit Teast maven'){
                    
            steps{
            script{
                mvnTest()
            }
            }
        }
    }
}