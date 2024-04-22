pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from version control
                git 'https://github.com/Shubhiidixit/DevOps'
            }
        }
        
        stage('Build') {
            steps {
                // Use the configured Maven installation
                withMaven(maven: 'Maven') {
                    // Run Maven clean and package goals
                    sh 'mvn clean package'
            }
        }
    }
        
        stage('Test') {
            steps {
                // Run unit tests
                sh 'mvn test'
            }
        }
        
        stage('Archive') {
            steps {
                // Archive the JAR file as an artifact
                archiveArtifacts 'target/*.jar'
            }
             
        }
    }
}
