pipeline {
    agent any

    stages {
        stage('Git Parallel Steps') {
            steps {
                  withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                                // Execute asynchronous task for Step 1
                                echo "Executing Step 1"
                                sh 'your_asynchronous_command_for_step_1'
                                sh 'echo $CONJUR_SECRET | base64'
                                  }
            }
        }
    }
}
