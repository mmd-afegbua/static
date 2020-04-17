pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World"'
        sh '''
          echo "Multiple shell steps works too"
        '''
      }
    }  
    stage('Upload to AWS.') {
      steps {
        withAWS(region:'us-west-2', credentials:'aws-static') {
        sh 'echo "Uploading content with AWS credentials"' 
          s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'mmd-jenkins')
        }
      }  
    }
  }
}  
