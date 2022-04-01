pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Cloning Git') {
      steps {
        git 'https://github.com/andreipope/HelloWorld'
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
     
    stage('Test') {
      steps {
         sh 'npm test'
        echo  $GOOGLE_PROJECT_ID > /tmp/CI_PIPELINE_ID.json
        cat  /tmp/CI_PIPELINE_ID.json
      }
    }      
  }
}
