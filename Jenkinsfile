pipeline {
    agent any

    //triggers {
        // Use to trigger the pipeline every minute
      //  pollSCM('* * * * *')
   // }

    stages {
        stage('conjur-credentials Main Branch') {
            steps {
               ////withCredentials([gitUsernamePassword(credentialsId: 'jenkins-username-password-cred', gitToolName: 'Default')]) {
                   withCredentials([conjurSecretCredential(credentialsId: 'github-credentials', variable: 'CONJUR_SECRET')]) {
                   ////withCredentials([conjurSecretUsername(credentialsId: 'git-multi-branch-conjur-credentials', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'sameer.shaik@cyberark')]) {
 
                   sh ' echo $CONJUR_SECRET | base64'
                
                }
            }
        }
    }
}
