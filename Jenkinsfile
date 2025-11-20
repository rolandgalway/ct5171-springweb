pipeline {
    agent any

    stages {
        stage('Check Java Version') {
            steps {
                sh 'echo JAVA VERSION:'
                sh 'java -version'
                sh 'echo MAVEN VERSION:'
                sh 'mvn -version'
            }
        }
        stage('Get Project') {
            steps {
                git url: 'https://github.com/rolandgalway/ct5171-springweb.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run Spring Boot') {
            steps {
                sh 'mvn spring-boot:run'
            }
        }

    }

}
