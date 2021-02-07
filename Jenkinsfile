pipeline {
   agent any
   stages {
    stage('Checkout') {
      steps {
        script {
           git url: 'https://github.com/szamashnoi1993/mytestapp.git'
           sh "ls -lart ./*" 
           sh "git branch -a"
           sh "git checkout master"
          }
       }
    }
    
    stage('build') {
        steps {
        script {
           sh 'make build'
            }
        }
    }


    stage('run') {
        steps{
            script {
                sh 'make run'
            }        
        }
    }
    
    
    }
}
