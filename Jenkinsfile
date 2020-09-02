node {
  
  stage('Code Checkout') {
    checkout scm
  }
  
  stage('Build Frontend'){
    sh "npm install"  
  }
  
  stage('Test frontend'){
    sh "npm run test"
  }  
  
  stage('Deploy frontend'){
    print "deploy frontend"
  }
 
}
