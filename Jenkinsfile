pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo 'build....'
            }
            steps {
                python testTrue.py
            }
            steps {
                python testFalse.py
            }
        }
        stage('Test') { 
            steps {
                echo 'test....'
            }
        }
        stage('Deploy') { 
            steps {
                echo 'deploy....'
            }
        }
    }
}
