pipeline {
    agent any
    
    tools {
        maven 'Maven'
    }
    parameters {
         string(name: 'Group2', defaultValue: '35.89.37.107', description: 'FeedbackMechanism')
    }

stages{
        stage("Build"){
            steps {
                sh 'clean package'
                echo "Building the project"
            }
            post {
                success {
                  emailext body: 'Email sent from Jenkins', subject: 'Test Email', to: 'berna075@csusm.edu'
                }
            }
        }
    }
}
