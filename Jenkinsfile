pipeline {
    agent any
    stages {
        /* "Build" and "Test" stages omitted */
        stage("Build"){
        }
        stage("Test"){
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
