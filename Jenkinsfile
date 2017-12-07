#!/usr/bin/env groovy
properties([
    [$class: 'GithubProjectProperty',
    displayName: '',
    projectUrlStr: 'https://github.com/MyFirstOrg-Jenkins/OrgProjRep2.git/'],
    pipelineTriggers([upstream(
    threshold: 'SUCCESS',
    upstreamProjects: 'https://github.com/MyFirstOrg-Jenkins/OrgProjRep1.git/'
    )])])

pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                sh 'pwd' 
            }
        }
        stage('Test'){
            steps {
                sh 'java -version'
                
            }
        }
        stage('Deploy') {
            steps {
                sh 'ls'
                sh 'pwd'
            }
        }
    }
}
