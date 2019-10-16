pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                 echo 'Hello Build !'
                 script{
                    def get = new URL("https://google.com").openConnection()
                    get.setRequestMethod("GET")
                    get.setDoOutput(true)
                    get.connect()
                    def response = get.content.text
                    return response
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

