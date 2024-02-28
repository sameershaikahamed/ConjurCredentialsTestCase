pipeline {
    agent any

    stages {
        stage('conjur-credentials Feature Branch') {
            steps {
               withCredentials([gitUsernamePassword(credentialsId: 'jenkins-username-password-cred', gitToolName: 'Default')]) {
               sh ' echo $jenkins-username-password-cred | base64'
                
                }
            }
        }
    }
}
