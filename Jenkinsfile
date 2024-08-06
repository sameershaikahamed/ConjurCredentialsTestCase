pipeline {
    agent any

    stages {
        stage('Folder Multi Branch Git Username & Password Credentials') {
            steps {
                withCredentials([gitUsernamePassword(credentialsId: 'github-username-credential', gitToolName: 'Default')]) {
                 sh 'echo $github-username-credential |bae64'
            }
                
            }
        }
    }
}
