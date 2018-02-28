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
                        echo 'build....'
                        bat 'python testTrue.py ${buildParam}'
                        sleep 5
                    }
                }
                stage('BuildStep2Use5s') { 
                    steps {
                        echo 'build....'
                        bat 'python testTrue.py ${build1Param}'
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
