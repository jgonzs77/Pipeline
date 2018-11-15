/*
pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                echo 'Building..'
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
*/
#!/usr/bin/env groovy
node {
    checkout scm
    stage('Build1'){
        echo 'Hola Mundo1'
        sh 'mvn compile'
    }
    stage('Test2') {
        echo 'Hola Mundo2'
        sh 'mvn test'
    }
    stage('Deploy3') {
        echo 'Hola Mundo3'
        sh 'mvn package'
    }
}
