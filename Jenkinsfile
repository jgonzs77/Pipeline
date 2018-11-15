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
        withMaven(maven:'Maven Test'){
            sh 'mvn test'
        }
        // junit '**/target/*.xml'
    }
    stage('Deploy3') {
        try{
            withMaven(maven:'Maven Test'){
            sh 'mvn package'
        } 
        }finally{
            //sh 'rm -rf $WORKSPACE'
            deleteDir()
        }
    }
}
