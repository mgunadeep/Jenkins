pipeline {
    agent any
    environment {
        CAR= "488-GTB"        // --> Pipeline variable
        NAME= "GUNA"
    }
    // triggers { cron('*/1 * * * *') }  --> for triggering the CRON jobs.
    // triggers { pollSCM('*/2 * 24 8 4') } --> for trigerring the pipelinejobs, if any git commits are done in the interval of every 2 minutes.

    stages {
        stage ('First task') {
            steps {
                echo "Hello World"
                echo "${CAR}"
            }
        }
        stage ('Second task') {
            environment {
            CAR= "TAYCAN"    // --> Stage variable
            }
            steps {
                sh ''' 
                echo "Hello "${NAME}", this is your "${CAR}" "
                ls -ltr
                pwd
                    '''
            }
        }
    }
}

// Here, the Stage(local) Variables > Pipeline(global) Variales.