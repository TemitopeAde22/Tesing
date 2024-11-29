pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M399"
    }

    stages {
        stage ("Hello") {
            steps {
                sh 'echo "Hello World"'
            }
        }
        stage('Check maven version') {
            steps {
               sh "echo print maven version"
               sh "mvn -version"
            }

            post {
                success {
                    sh "echo The build was sucessful"
                
                }
                failure {
        echo 'This runs on failure'
    }
              
            }
        }
    }
}
