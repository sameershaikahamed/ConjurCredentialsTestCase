pipeline {
    agent any

    stages {
        stage('BitBucket-Git URL Conjur Secret') {
            steps {
                 script{
                    varVal =null
                withCredentials([conjurSecretCredential(credentialsId: 'bitbucket-sonarqube-multi-branch-folder-job-credential1', variable: 'CONJUR_SECRET')]) {
                    
                    varVal= CONJUR_SECRET
                    
                }
                  echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
               
            }
        }
      
            stage('Folder-1-Folder Job-Conur-Secret Username-Credentials') {
            steps {
                script{
                    varVal =null
             withCredentials([conjurSecretUsername(credentialsId: 'SONARQUBE-BITBUCKET-CONJUR_CRED-USERNAME-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
            }
        }
    }
}
