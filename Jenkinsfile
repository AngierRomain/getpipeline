pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                 echo 'Hello Build !' 

                 @Test
                 void make_get_request() {
                     def http = new HTTPBuilder()
                        http.request( 'http://www.leveluplunch.com', Method.GET, ContentType.TEXT ) { req ->
                        uri.path = '/groovy/examples/'
                        headers.'User-Agent' = "Mozilla/5.0 Firefox/3.0.4"
                        headers.Accept = 'application/json'
                
                        response.success = { resp, reader ->
                            assert resp.statusLine.statusCode == 200
                            println "Got response: ${resp.statusLine}"
                            println "Content-Type: ${resp.headers.'Content-Type'}"
                            println reader.text
                        }
                
                        response.'404' = {
                            println 'Not found'
                        }
                    }
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