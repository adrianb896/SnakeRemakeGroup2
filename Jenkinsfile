pipeline {
    agent any
    
    tools {
        maven 'local_maven'
    }
    parameters {
         string(name: 'Group2', defaultValue: '35.89.37.107', description: 'Feedback Mechanism')
    }

stages{
        stage("Build"){
            steps {
                sh 'clean package'
                echo "Building the project"
            }
            post {
                success {
                  emailext body: 'Email sent from Jenkins', subject: 'Test Email', to: 'se481group2@gmail.com'
                }
            }
        }
    }
}
