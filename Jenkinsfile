pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'JDK21'
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build & Deploy to Nexus') {
            steps {
                sh 'mvn -B clean deploy -DskipTests'
            }
        }
    }
}
