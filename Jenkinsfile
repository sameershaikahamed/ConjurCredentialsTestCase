pipeline {
    agent any

    stages {
        stage('BitBucket-Git URL Conjur Secret') {
            steps {
                 script{
                    varVal =null
                withCredentials([conjurSecretCredential(credentialsId: 'BITBUCKET-SONAR-CONJUR-CRED-ID', variable: 'CONJUR_SECRET')]) {
                    
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
             withCredentials([conjurSecretUsername(credentialsId: 'BITBUCKET-GIT-REPO-Conjur-USERNAME-PWD-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
            }
        }
    }
}
