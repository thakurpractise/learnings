pipeline {
    agent any
    stages {
        stage( 'clone repo') {
            steps {
                sh "git status"
                sh " git clone https://github.com/thakurpractise/learnings.git "
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
    }
}
