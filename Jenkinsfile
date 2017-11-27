pipeline {
    agent any
    stages {
               stage("Build"){
            steps {
                echo('building')
            }
        }
        stage("Test"){
            steps {
                echo('Testing')
            }
        }
        stage('Deploy - Staging') {
            steps {
                echo('./deploy staging')
                echo('./run-smoke-tests')
            }
        }

        stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }

        stage('Deploy - Production') {
            steps {
                echo('./deploy production')
            }
        }
    }
}

