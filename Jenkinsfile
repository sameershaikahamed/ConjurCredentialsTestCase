pipeline {
    agent any

    stages {
        stage('conjur-credentials Main Branch') {
            steps {
               withCredentials([gitUsernamePassword(credentialsId: 'jenkins-username-password-cred', gitToolName: 'Default')]) {
                   //withCredentials([conjurSecretUsername(credentialsId: 'git-multi-branch-conjur-credentials', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'sameer.shaik@cyberark')]) {
 
               sh ' echo $jenkins-username-password-cred | base64'
                
                }
            }
        }
    }
}
