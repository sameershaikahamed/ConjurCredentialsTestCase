pipeline {
    agent any

    stages {
    stage('API KEY Conjur Cred ') {
            steps {
             script{
                    user =null
 
                   /// withCredentials([conjurSecretCredential(credentialsId: 'apikey-username-cred', variable: 'CONJUR_SECRET')]) {
                 withCredentials([conjurSecretCredential(credentialsId: 'apikey-username', variable: 'CONJUR_SECRET')]) {
                      user=CONJUR_SECRET
                }
                echo " API KEY URL : ${user}"
                }
            }
        }
        
           stage('API KEY Conjur Username Cred ') {
            steps {
             script{
                    user =null
 
                   /// withCredentials([conjurSecretCredential(credentialsId: 'apikey-username-cred', variable: 'CONJUR_SECRET')]) {
               withCredentials([conjurSecretUsername(credentialsId: 'APIKEY-USERNAME-CONJUR-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                      user=CONJUR_SECRET
                }
                echo " API KEY URL : ${user}"
                }
            }
        }
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
