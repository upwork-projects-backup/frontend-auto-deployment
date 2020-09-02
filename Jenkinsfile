node {
  
  stage('Code Checkout') {
    checkout scm
  }
  
  stage('Build Frontend'){
    sh "npm install"  
  }
  
  stage('Deploy frontend'){
    sh "deploy frontend"
  }
 
}
