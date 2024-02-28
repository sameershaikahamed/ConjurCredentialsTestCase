pipeline {
    agent any

    stages {
        stage('conjur-credentials Main Branch') {
            steps {
                withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
               sh ' echo $CONJUR_SECRET | base64'
                
                }
            }
        }
    }
}
