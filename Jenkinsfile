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

           stage('Git-Folder-level-Job-Jenkins-Credentials') {
            steps {
                script{
                    varVal =null
                    varPwd =null
                withCredentials([usernamePassword(credentialsId: 'folder-level-username-pwd-ID', passwordVariable: 'pwd', usernameVariable: 'username')]) {
                        varVal = username
                        varPwd = pwd
                    }
                echo "Folder-1-Jenkins Cred Val User : ${varVal}"
                  echo "Folder-1-Jenkins  Cred Val pwd : ${varPwd}"
                }
            }
        }
        
          
    }
}

