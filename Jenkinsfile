pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                 echo 'Hello Build !'
                 script{
                    curl -I "www.google.com" 
                 }   
            }
        }

        stage('Test') { 
            steps {
                echo 'Hello Test !'
            }
        }

        stage('Deploy') { 
            steps {
                 echo 'Hello Deploy !'
            }
        }
    }
}

