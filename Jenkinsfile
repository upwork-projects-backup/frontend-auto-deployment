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
    withCredentials([sshUserPrivateKey(credentialsId: "scp-credential", keyFileVariable: 'keyfile')]) {
      sh """
      scp -i ${keyfile} \
        -rp app azureuser@52.165.33.103:/serv/
      """
    }
  } 
  
}
