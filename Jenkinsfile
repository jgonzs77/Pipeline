pipeline {
    agent any
    checkout scm
    tools {
        maven 'Maven Test'
    }
    stages {
        stage('Build'){
            steps {
                echo 'Building..'
                sh 'mvn --version'
               /* sh '/usr/bin/git config remote.origin.url https://github.com/IvanciniGT/maven-test-repository' */
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
            }
        }
    }
    
}
