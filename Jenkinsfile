pipeline {
    agent any

    stages {
        stage('Parallel Steps') {
            parallel {
                stage('Step 1') {
                    steps {
                        script {
                            try {
                                  withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                                // Execute asynchronous task for Step 1
                                echo "Executing Step 1"
                                sh 'your_asynchronous_command_for_step_1'
                                sh 'echo $CONJUR_SECRET | base64'
                                  }
                            } catch (Exception e) {
                                // Handle error for Step 1
                                error("Error occurred in Step 1: ${e.message}")
                            }
                        }
                    }
                }
                stage('Step 2') {
                    steps {
                        script {
                            try {
                                 withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                                // Execute asynchronous task for Step 2
                                echo "Executing Step 2"
                                sh 'your_asynchronous_command_for_step_2'
                                sh 'echo $CONJUR_SECRET | base64'
                                 }
                            } catch (Exception e) {
                                // Handle error for Step 2
                                error("Error occurred in Step 2: ${e.message}")
                            }
                        }
                    }
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline execution failed'
        }
    }
}
