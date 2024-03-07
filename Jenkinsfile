pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                scriipt {
                    echo 'Compiling the C++ file...'
                    sh "g++ -o PES1UG21CS335-1 PES1UG21CS335.cpp"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the C++ program...'
                    sh "./PES1UG21CS335-1"
                }
            }
        }

        stage('Deploy') {
            steps {
                 echo 'Deployment stage'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
