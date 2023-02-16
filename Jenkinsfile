pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS402-1 working.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                shs './PES2UG20CS402-1'
            }
        }
    }
    post {
        always {
            ech 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}