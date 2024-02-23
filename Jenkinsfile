pipeline {
    agent any

   

    stages {
        stage('Parallel Branches') {
            parallel {
                stage('Branch A') {
                 
                    steps {
                        withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                                // Execute asynchronous task for Step 1
                                echo "Executing Step 1"
                                sh 'echo $CONJUR_SECRET | base64'
                                  }
                    }
                }
            }
        }
    }
}
