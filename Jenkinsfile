pipeline {
    agent any

    stages {
        stage('Multibranch-Git-Conur-Credentials') {
            steps {
                script{
                    varVal =null
                //withCredentials([conjurSecretCredential(credentialsId: 'intel-multi-folder-job-credential1', variable: 'CONJUR_SECRET')]) {
                     withCredentials([conjurSecretCredential(credentialsId: 'intel-multi-folder-job-credential1', variable: 'CONJUR_SECRET')]) {
                   // withCredentials([conjurSecretCredential(credentialsId: 'no-folder-bitbucket-credential1', variable: 'CONJUR_SECRET')]) {
                  

                        varVal = CONJUR_SECRET
                     //sh 'echo Folder-1-Conjur Bitbucket Conjur Cred Cred Val '
                    }
                echo "Folder-1-Conjur Bitbucket Conjur Cred Cred Val  : ${varVal}"
                }
            }
        }
      
        /* stage('Multibranch-Git-Conur-Secret-Username-Credentials') {
            steps {
                script{
                    varVal =null
                  withCredentials([conjurSecretUsername(credentialsId: 'Conjur-USERNAME-INTEL-FOLDER-JOB-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                                       //  withCredentials([conjurSecretUsername(credentialsId: 'standalone-username-conjur-secret-username-IDO', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                        
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Bitbucket Conjur Secret Username Cred Val  : ${varVal}"
                }
            }
        }*/
      
    }
}
