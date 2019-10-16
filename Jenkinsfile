pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                 echo 'Hello Build !'
                 def get = new URL("https://httpbin.org/get").openConnection();
                 def getRC = get.getResponseCode();
                 println(getRC);
                 if(getRC.equals(200)) {
                 println(get.getInputStream().getText());
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

