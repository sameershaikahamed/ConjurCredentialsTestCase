pipeline {
    agent any

    stages {
        stage('Git Conjur Credentials') {
            steps {
                script{
                    varVal =null
                withCredentials([conjurSecretCredential(credentialsId: 'jenkins-app-dbPassword', variable: 'CONJUR_SECRET')]) {
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
                withCredentials([conjurSecretUsername(credentialsId: 'APIKey-username-ID', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
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
                withCredentials([usernamePassword(credentialsId: 'global-username-pwd-jenkins-credentials-ID', passwordVariable: 'pwd', usernameVariable: 'username')]) {
                        varVal = pwd
                    }
                echo "Job-Jenkins Cred Val  : ${varVal}"
                }
            }
        }
        
          
    }
}
