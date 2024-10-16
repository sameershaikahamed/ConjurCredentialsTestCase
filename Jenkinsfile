pipeline {
    agent any

    stages {
        stage('Multibranch-bitbucket-Conur-Credentials') {
            steps {
                script{
                    varVal =null
                withCredentials([conjurSecretCredential(credentialsId: 'multi-branch-level-standalone-credential1', variable: 'CONJUR_SECRET')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Bitbucket Conjur Cred Cred Val  : ${varVal}"
                }
            }
        }

            stage('Multibranch-bitbucket-Conur-Secret-Username-Credentials') {
            steps {
                script{
                    varVal =null
                    withCredentials([conjurSecretUsername(credentialsId: 'bitbucket-conjut-credentials-IDDDD', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Bitbucket Conjur Secret Username Cred Val  : ${varVal}"
                }
            }
        }
    }
}
