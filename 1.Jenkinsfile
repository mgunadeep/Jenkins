pipeline {
    agent any
    environment {
        CAR= "488 GTB"
        NAME= "GUNA"
    }
    stages {
        stage ('First task') {
            steps {
                echo "Hello World"
                echo "${CAR}"
            }
        }
        stage ('Second task') {
            environment {
            CAR= "TAYCAN"
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