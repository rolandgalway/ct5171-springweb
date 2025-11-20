pipeline {
    agent any

    stages {

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
