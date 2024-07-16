pipeline {
    agent any

    //triggers {
        // Use to trigger the pipeline every minute
      //  pollSCM('* * * * *')
   // }

    stages {
        stage('Folder Multi Brach Git Username & Password Credentials ) {
            steps {
                withCredentials([conjurSecretCredential(credentialsId: 'multi-folder-multi-branch-username-pwd-credentials', variable: 'CONJUR_SECRET')]) {
                 //withCredentials([gitUsernamePassword(credentialsId: 'test-multibranch-pipeline-credential1', gitToolName: 'Default')]) {
                   //withCredentials([conjurSecretCredential(credentialsId: 'test-multibranch-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                  //withCredentials([conjurSecretUsername(credentialsId: 'test-multibranch-pipeline-credential1', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'sameer.shaik@cyberark')]) {
 
                   sh ' echo $CONJUR_SECRET | base64'
                
                }
            }
        }

                    stage('Folder Multi Brach Git Repository with  Username & Password Credentials ) {
            steps {
                 git url: 'https://github.com/sameershaikahamed/ConjurCredentialsTestCase.git',
                    credentialsId: 'multi-folder-multi-branch-username-pwd-credentials'
                
                }
            
        }

       
    }
}
