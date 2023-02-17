pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ task5_318.cpp -o task5_318'
                 build job: 'PES1UG20CS318-1', wait: false
                 echo 'Build successful'
            }
        }

        stage('Test') {
            steps {
                sh './task5_318'
                echo 'Test successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
