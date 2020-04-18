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
    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }  
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-west-2', credentials:'aws-static') {
          s3Upload(file:'index.html', bucket:'mmd-jenkins')
        }
      }
    }  
  }
}  
