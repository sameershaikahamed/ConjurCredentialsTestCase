pipeline {
    agent any

    stages {
        stage('Multibranch-bitbucket-Conur-Credentials') {
            steps {
                script{
                    varVal =null
                withCredentials([conjurSecretCredential(credentialsId: 'intel-multi-branch-folder-job-credential1', variable: 'CONJUR_SECRET')]) {
                   // withCredentials([conjurSecretCredential(credentialsId: 'no-folder-bitbucket-credential1', variable: 'CONJUR_SECRET')]) {
                  

                        varVal = CONJUR_SECRET
                     //sh 'echo Folder-1-Conjur Bitbucket Conjur Cred Cred Val '
                    }
                echo "Folder-1-Conjur Bitbucket Conjur Cred Cred Val  : ${varVal}"
                }
            }
        }
      
         stage('Multibranch-bitbucket-Conur-Secret-Username-Credentials') {
            steps {
                script{
                    varVal =null
                    withCredentials([conjurSecretUsername(credentialsId: 'intel-bitbucket-conjur-credentials-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Bitbucket Conjur Secret Username Cred Val  : ${varVal}"
                }
            }
        }
      
    }
}
