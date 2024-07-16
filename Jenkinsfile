pipeline {
    agent any

    // Uncomment the following section to trigger the pipeline every minute
    // triggers {
    //     pollSCM('* * * * *')
    // }

    stages {
        stage('Folder Multi Branch Git Username & Password Credentials') {
            steps {
                withCredentials([conjurSecretCredential(credentialsId: 'multi-folder-multi-branch-username-pwd-credentials', variable: 'CONJUR_SECRET')]) {
                    sh 'echo $CONJUR_SECRET | base64'
                }
            }
        }

        stage('Folder Multi Branch Git Repository with Username & Password Credentials') {
            steps {
                git url: 'https://github.com/sameershaikahamed/ConjurCredentialsTestCase.git',
                    credentialsId: 'multi-folder-multi-branch-username-pwd-credentials'
            }
        }
    }
}
