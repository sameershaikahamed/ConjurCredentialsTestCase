pipeline {
    agent any

    stages {
        stage('Folder Multi Branch Git Username & Password Credentials') {
            steps {
                withCredentials([gitUsernamePassword(credentialsId: 'multi-folder-multi-branch-username-pwd-credentials', gitToolName: 'Default')]) {
                 sh 'echo $github-username-credential |base64'
            }
                
            }
        }
    }
}
