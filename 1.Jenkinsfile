pipeline {
    agent any
    environment {
        CAR= "488 GTB"        // Pipeline variable
        NAME= "GUNA"
    }
    triggers { cron('1 * * * *') }
    stages {
        stage ('First task') {
            steps {
                echo "Hello World"
                echo "${CAR}"
            }
        }
        stage ('Second task') {
            environment {
            CAR= "TAYCAN"    // Stage variable
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