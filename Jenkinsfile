pipeline{
    agent any

    environment{
        ON_SUCCESS_SEND_EMAIL = true
        ON_FAILURE_SEND_EMAIL = true
    }

    stages{
        stage('Build'){
            steps{
                echo 'Building'
                bat 'mvn install --file ./backend'
                bat 'npm install --prefix ./frontend'

            }
        }
        stage('Test'){
            steps{
                echo 'Testing'
            }
        }
    }
}