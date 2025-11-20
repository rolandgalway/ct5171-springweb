=====================================================

Jenkins Pipeline: from Get to Exec (below)

=====================================================

pipeline {
    agent any
    stages {
        stage ('GetProject') {
            steps {
                git 'https://github.com/rolandgalway/ct5171-springweb.git'
            }
        }
        stage ('build') {
            steps {
                sh 'mvn clean:clean'
                sh 'mvn dependency:copy-dependencies'
                sh 'mvn compiler:compile'
            }
        }
        stage ('Exec') {
            steps {
                sh 'mvn exec:java'
            }
        }
}