pipeline {
    agent any

    stages {
        stage('Global Conjur Secret Credentials') {
            steps {
                script{
                    user=null
                    pwd=null
                    withCredentials([conjurSecretCredential(credentialsId: 'GlobalCredentials-job-credential1', variable: 'CONJUR_SECRET')]) {
                    // some block
                    //user = USERNAME
                    pwd = CONJUR_SECRET
                    
                }
                //echo "API KEY USERNAME =${user}"
                echo "Global Conjur Secret Credentials  =${pwd}"
                }
            }
        }
    }
}
