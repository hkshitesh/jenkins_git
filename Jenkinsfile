pipeline {
    agent {
        label 'master'
    }
    stages {
        stage('S1') {
            steps {
                echo "Hello"
            }
        }
        stage('S2') { 
            steps {
                echo 'mvn test' 
            }
        stage('S3') { 
            steps {
                sh 'mvn clean' 
            }
            post {
                always {
                    echo 'mvn test'
                }
            }
        }
    }
}
