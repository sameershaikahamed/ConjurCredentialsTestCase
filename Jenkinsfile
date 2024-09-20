pipeline {
    agent any

    stages {
        stage('Git Conjur Credentials') {
            steps {
                script{
                    varVal =null
                withCredentials([conjurSecretCredential(credentialsId: 'folder-1-regression-credential1', variable: 'CONJUR_SECRET')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
            }
        }
    
           stage('Git  Conur Secret Username Credentials') {
            steps {
                script{
                    varVal =null
                withCredentials([conjurSecretUsername(credentialsId: 'folder-2-job-conjursecretusername-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
            }
        }
        
         stage('Git-Username Credentials') {
            steps {
                script{
                    varVal =null
                withCredentials([usernamePassword(credentialsId: 'github-username-credential', passwordVariable: 'pwd', usernameVariable: 'username')]) {
                        varVal = pwd
                    }
                echo "Job-Jenkins Cred Val  : ${varVal}"
                }
            }
        }
        
          
    }
}

