pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo 'build....'
                bat 'python testTrue.py'
                bat 'python testFalse.py'
            }
            //steps {
            //    python testTrue.py
            //}
            //steps {
            //    python testFalse.py
           // }
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
