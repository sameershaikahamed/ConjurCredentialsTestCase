pipeline {
    agent any

    stages {
        stage('conjur-credentials test-mbp-branch') {
            steps {
               withCredentials([gitUsernamePassword(credentialsId: 'jenkins-username-password-cred', gitToolName: 'Default')]) {
               sh ' echo $jenkins-username-password-cred | base64'
                
                }
            }
        }
    }
}
