pipeline {
    agent any

    environment {
    ENV = "www.twitter.com"  // Pipeline variable 
    }

    stages {
        stage ('first task') {
            steps {
             echo "Introduction to Jenkins"
             echo "${ENV}"
            }
        }
        stage ('Second task') {
            environment {
                ENV = "www.facebook.com"   // Stage variable
            }
            steps {
                echo "Configuring a Jenkinsfile"
                echo "${ENV}"
            }
        }
        stage ('Third task') {
            steps {
                sh '''echo Jenkins is Ready
                    ls -ltra
                    pwd
                    ps -ef | grep Jenkins'''
                    echo "${ENV}"
            }
        }
    }
}


//





