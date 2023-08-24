pipeline {
    agent any

    environment {
    ENV = "www.twitter.com"             // Pipeline variable 
    SSHCRED= ('SSH_CRED')
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'GUNA', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
                ENV = "www.facebook.com"   
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


 





