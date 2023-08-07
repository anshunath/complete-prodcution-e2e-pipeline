@Library ('jenkins_shared_lib')
pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                Script{
                    gitCheckuot(
                        branch: "main"
                        url: "https://github.com/anshunath/jenkins_shared_lib.git"
                    )
                }
                
            }
        }
    }
}