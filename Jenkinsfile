pipeline{
    agent any
    tools{
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
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
        stage("Test Application"){
            steps {
                sh "mvn test"
            }

        }
        stage("Sonarqube Analysis") {
            steps {
                script {
                    withSonarQubeEnv(credentialsId: 'sonar-api') {
                        sh "mvn sonar:sonar"
                    }
                }
            }

        }
        stage("Quality Gate") {
            steps {
                script {
                    //waitForQualityGate abortPipeline: false, credentialsId: 'sonar-api'
                }
            }

        }
    }
}