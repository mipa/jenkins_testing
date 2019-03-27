pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                sh "rm -rf springExample"
                sh "git clone https://github.com/ravikiran-srini/springExample.git"
                sh "mvn clean -f springExample"
            }
        }
        stage('Test'){
            steps {
                sh "mvn test -f springExample"
            }
        }
        stage('Deploy'){
            steps {
                 sh "mvn package -f springExample"
            }
        }
    }
}
