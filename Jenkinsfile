pipeline {
    agent any
    environment {
        buildParam = 'buildParam1'
        build1Param = 'buildParam2'
    }
    stages {
        stage('Build') {
            parallel {
                stage('BuildStep1Use5s') { 
                    steps {
                        echo 'build.... ${buildParam}'
                        bat 'python testTrue.py'
                        sleep 5
                    }
                }
                stage('BuildStep2Use5s') { 
                    steps {
                        echo 'build.... ${build1Param}'
                        bat 'python testTrue.py'
                        sleep 5
                    }
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
