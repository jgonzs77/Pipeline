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
//  #!/usr/bin/env groovy
node {
    checkout scm
    stage('Build1'){
        withMaven(maven:'Maven Test'){
            sh 'mvn compile'
        }
    }
    stage('Test2') {
        sh 'mvn test'
    }
    stage('Deploy3') {
        sh 'mvn package'
    }
}
