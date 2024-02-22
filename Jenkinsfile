pipeline {
    agent any

    stages {
        stage('Parallel Branches') {
            parallel {
                stage('Branch A') {
                    when {
                        branch 'main'
                    }
                    steps {
                        withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                                // Execute asynchronous task for Step 1
                                echo "Executing Step 1"
                                sh 'echo $CONJUR_SECRET | base64'
                                  }
                    }
                }
                stage('Branch B') {
                    when {
                        branch 'dev-branch'
                    }
                    steps {
                          withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                                // Execute asynchronous task for Step 1
                                echo "Executing Step 1"
                                sh 'echo $CONJUR_SECRET | base64'
                                  }
                    }
                }
                // Add more stages for additional branches as needed
            }
        }
    }
}
