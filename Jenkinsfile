pipeline {

  agent any
  
  stages{
    stage ("Build"){
      steps{
        echo "Building the project"
      }
    }
    post {
      success{
      emailext body: 'Email sent from Jenkins', subject: 'Test Email', to: 'adrianbernardino02@gmail.com'
      }
    }
  }
}
