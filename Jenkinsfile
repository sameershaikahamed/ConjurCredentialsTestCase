pipeline {
    agent any

    stages {
        stage('conjur-credentials Main Branch') {
            steps {
               ///withCredentials([gitUsernamePassword(credentialsId: 'jenkins-username-password-cred', gitToolName: 'Default')]) {
                   withCredentials([conjurSecretCredential(credentialsId: 'multi-pipeline-job-credential1', variable: 'CONJUR_SECRET')]) {
                   ///withCredentials([conjurSecretUsername(credentialsId: 'git-multi-branch-conjur-credentials', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'sameer.shaik@cyberark')]) {
 
                   sh ' echo $CONJUR_SECRET | base64'
                
                }
            }
        }
    }
}
