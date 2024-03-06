pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile hello.cpp
                sh 'g++ -o hello hello.cpp'
            }
        }
        stage('Test') {
            steps {
                // Run hello.cpp
                sh './hello'
            }
        }
    }

    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
