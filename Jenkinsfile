pipeline {
    agent any

    environment {
    ENV = "www.twitter.com"             // Pipeline variable 
    SSHCRED= ('SSH_CRED')

    }
    triggers { cron('H 1 * * 8 *') }
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
                      ps -ef | grep Jenkins
                      ls -ltra
                      pwd
                      echo "${ENV}"

                      env
                   '''
            }
        }
        stage ('Fourth task') {
            steps {
                sh '''echo -e "\\e[32m Hello world \\e[0m"
                      echo -e "\\e[36m I love this color \\e[0m"
                   '''
            }
        }
    }
}


// Here, the Stage(local) Variables > Pipeline(global) Variales, 





