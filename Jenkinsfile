pipeline {
    agent any

    stages {
        stage('Compile Stage') {

            steps {
                withMaven(maven : 'MAVEN 3.8.4') {
                    sh 'mvn clean complie'
                }
            }
        }

        stage('Testing ') {

            steps {
                withMaven(maven: 'MAVEN 3.8.4') {
                    sh 'mvn test'
                }
            }
        }

        stage('Deployment Stage') {
            steps {
                withMaven(maven: 'MAVEN 3.8.4') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
