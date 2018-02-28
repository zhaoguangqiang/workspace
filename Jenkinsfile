pipeline {
    agent any
    stages {
        stage('Build') {
            environment {
                buildParam = 'buildParam1'
                build1Param = 'buildParam2'
            }
            parallel {
                stage('BuildStep1Use5s') { 
                    steps {
                        echo "build.... ${buildParam}"
                        bat "python testTrue.py ${buildParam}"
                        sleep 5
                    }
                }
                stage('BuildStep2Use5s') { 
                    steps {
                        echo "build.... ${build1Param}"
                        bat "python testTrue.py ${build1Param}"
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
