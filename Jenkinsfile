pipeline {
    agent { label 'agent-1' }
    
    tools {
        maven 'maven3.9'
        jdk 'jdk17'
    }

    stages {
        
        stage('Clone') {
            steps {
             git branch: 'main', url: 'https://github.com/meer1555/board-game.git'
            }
        }
        stage('Compile') {
            steps {
             sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
               sh 'mvn package'
            }
        }
    }
}
