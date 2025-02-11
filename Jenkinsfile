pipeline {
    agent any

    stages {
        stage('BitBucket-Git URL Conjur Secret') {
            steps {
                 script{
                    varVal =null
                withCredentials([conjurSecretCredential(credentialsId: 'folder-2-regression-credential1', variable: 'CONJUR_SECRET')]) {
                    
                    varVal= CONJUR_SECRET
                    
                }
                  echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
               
            }
        }

        
            /*stage('Jenkins Multi Branch Folder-1-Folder Job-Conur-Secret Username-Credentials') {
            steps {
                script{
                    varVal =null
              withCredentials([conjurSecretUsername(credentialsId: 'Folder2-Conjur-Username-PWD-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
            }
        }*/

         stage('Jenkins Folder-1-Folder Job-Conur-Secret Username-Credentials') {
            steps {
                script{
                    varVal =null
              
        withCredentials([conjurSecretUsername(credentialsId: 'Intel-Folder-Job-Cred-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
            }
        }
      
            /*stage('Folder-1-Folder Job-Conur-Secret Username-Credentials') {
            steps {
                script{
                    varVal =null
             withCredentials([conjurSecretUsername(credentialsId: 'BITBUCKET-GIT-REPO-Conjur-USERNAME-PWD-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                        varVal = USERNAME
                    }
                echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
            }
        }*/
    }
}
