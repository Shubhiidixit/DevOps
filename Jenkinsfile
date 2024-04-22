pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout source code from version control
                git 'https://github.com/ricky2129/todo-list-java'
            }
        }
        
        stage('Build') {
            steps {
                // Compile Java code and package it into a JAR file
                sh 'mvn clean package'
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
