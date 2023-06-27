@Library('Jenkins-shared-library') _
pipeline{

    agent any

    

    stages{
         
        stage('Git Checkout'){
                    
            steps{
            script{
                git branch: 'main', url: 'https://github.com/anshunath/complete-prodcution-e2e-pipeline.git'
            }
            }
        }
        
    }
}