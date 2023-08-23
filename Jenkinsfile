pipeline {
    agent any

    environment{
    ENV= "www.twitter.com"
    }

    stages {
        stage ('first task') {
            steps {
             echo "Introduction to Jenkins"
             echo "${ENV}"
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








