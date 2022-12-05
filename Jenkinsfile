pipeline {
    agent any
    
    tools {
        maven 'local_maven'
    }
    parameters {
         string(name: 'group2', defaultValue: '35.89.37.107', description: 'Remote Staging Server')
    }

stages{
        stage("Build"){
            steps {
                sh 'mvn clean package'
                echo "Building the project"
            }
            post {
                success {
                  emailext body: 'Email sent from Jenkins', subject: 'Test Email', to: 'adrianbernardino02@gmail.com'
                }
            }
        }
    }
}
