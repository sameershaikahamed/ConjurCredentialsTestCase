pipeline {
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
}
