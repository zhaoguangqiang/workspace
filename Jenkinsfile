pipeline {
    agent any 
    stages {
        parallel {
            stage('BuildStep1Use5s') { 
                steps {
                    echo 'build....'
                    bat 'python testTrue.py'
                    sleep 5
                }
            }
            stage('BuildStep2Use5s') { 
                steps {
                    echo 'build....'
                    bat 'python testFalse.py'
                    sleep 5
                }
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
