pipeline{
    agent any
    tools{
        jdk 'Java9'
        maven 'Maven3'
    }
    stages{
        stage("Cleanup Workspace"){
            steps {
                cleanWs()
            }

        }
    
        stage("Checkout from SCM"){
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/anshunath/complete-prodcution-e2e-pipeline'
            }

        }

        stage("Build Application"){
            steps {
                sh "mvn clean package"
            }

        }
    }
}