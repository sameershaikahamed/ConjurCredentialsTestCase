pipeline {
    agent any

    //triggers {
        // Use to trigger the pipeline every minute
      //  pollSCM('* * * * *')
   // }

    stages {
        stage('conjur-credentials Main Branch') {
            steps {
                //withCredentials([conjurSecretCredential(credentialsId: 'multi-folder-multi-branch-username-pwd-credentials', variable: 'CONJUR_SECRET')]) {
                    withCredentials([gitUsernamePassword(credentialsId: 'multi-folder-multi-branch-username-pwd-credentials', gitToolName: 'Default')]) {
                 //withCredentials([gitUsernamePassword(credentialsId: 'test-multibranch-pipeline-credential1', gitToolName: 'Default')]) {
                   //withCredentials([conjurSecretCredential(credentialsId: 'test-multibranch-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                  //withCredentials([conjurSecretUsername(credentialsId: 'test-multibranch-pipeline-credential1', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'sameer.shaik@cyberark')]) {
 
                   sh ' echo $multi-folder-multi-branch-username-pwd-credentials | base64'
                
                }
            }
        }
    }
}
