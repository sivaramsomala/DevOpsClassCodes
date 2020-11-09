pipeline {
    agent any

    stages {
    stage ('Compile stage')
        steps{
            withMaven(maven: 'Maven') {
                sh 'mvn clean compile'
                }
            }
        stage ('Testing Stage') {
            steps {
                withMaven(maven: 'Maven') {
                    sh 'mvn test'
                }
            }
        }
        stage ('Package Stage') {
            steps {
                withMaven(maven: 'Maven') {
                    sh 'mvn package'
                }
            }
        }
            
    }
}
