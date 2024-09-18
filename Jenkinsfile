pipeline {
    agent any

    stages {
        stage('Multibranch-Git-Conur-Credentials') {
            steps {
                script{
                    varVal =null
                withCredentials([conjurSecretCredential(credentialsId: 'no-folder-bitbucket-credential1', variable: 'CONJUR_SECRET')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Bitbucket  Cred Val  : ${varVal}"
                }
            }
        }
    }
}
