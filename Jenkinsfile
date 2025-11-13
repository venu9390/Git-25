pipeline {
    agent any
    tools {
        maven 'maven3.9.10'
        jdk 'java17'
    }
    stages {
        stage ('checkuot') {
            steps {
                git branch: 'main' , url: 'https://github.com/venu9390/Git-25.git'
            }
        }
        stage ('build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage ('publish to nexus') {
            steps {
                sh 'mvn deploy'
            }
        }
        stage ('post build') {
            steps {
                echo "Build and publish completed successfully "
            }
        }
    }

}
