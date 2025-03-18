pipeline {
    agent any
    stages {
      
        stage('Build') {
            steps {
                script {
                    build 'PES1UG22CS694-1'
                    sh 'g++ -o meow main/hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './meow'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'This is deploying yay !'
            }
        }
    }

    post {
        failure {
            echo 'Bruh you made an error lol. Pipeline has failed'
        }
    }
}
