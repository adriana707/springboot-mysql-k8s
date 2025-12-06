pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Jenkins will use the Git settings you configured for this job
                checkout scm
            }
        }

        stage('Build & Deploy to Nexus') {
            steps {
                // This uses your pom.xml (with distributionManagement) to deploy to Nexus
                sh 'mvn -B clean deploy -DskipTests'
            }
        }
    }
}

