pipeline {
    agent any
    stages {
        stage ('first task') {
            steps {
             echo "Introduction to Jenkins"
            }
        }
        stage ('Second task') {
            steps {
                echo "Configuring a Jenkinsfile"
            }
        }
        stage ('Third task') {
            steps {
                sh '''echo Jenkins is Ready
                    ls -ltra
                    pwd
                    ps -ef | grep Jenkins'''
            }
        }
    }
}








