/*pipeline {
    agent any

    // Uncomment the following section to trigger the pipeline every minute
    // triggers {
    //     pollSCM('* * * * *')
    // }

    stages {
        stage('Folder Multi Branch Git Username & Password Credentials') {
            steps {
                    withCredentials([gitUsernamePassword(credentialsId: 'multi-folder-multi-branch-username-pwd-credentials', gitToolName: 'Default')]) {
                    sh 'echo $multi-folder-multi-branch-username-pwd-credentials | base64'
                }
            }
        }

        stage('Folder Multi Branch Git Repository with Username & Password Credentials') {
            steps {
                git url: 'http://github.com/sameershaikahamed/ConjurCredentialsTestCase.git',
                    credentialsId: 'multi-folder-multi-branch-username-pwd-credentials',
                    branch: 'main'
            }
        }
    }
}*/

pipeline {
    agent any

    //triggers {
        // Use to trigger the pipeline every minute
      //  pollSCM('* * * * *')
   // }

    stages {
        stage('Folder Multi Brach Git Username & Password Credentials ) {
            steps {
                withCredentials([conjurSecretCredential(credentialsId: 'folder1-username-pwd-dummy-cred', variable: 'CONJUR_SECRET')]) {
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
}

