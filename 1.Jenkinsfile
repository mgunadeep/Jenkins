pipeline {
    agent any
    environment {
        ENV= "488 GTB"
        
    }
    stages {
        stage ('First task') {
            steps {
                echo "Hello World"
                echo "${ENV}"
            }
        }
    }
}