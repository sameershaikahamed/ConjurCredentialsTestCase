pipeline {
    agent any

   

    stages {
        stage('Parallel Branches') {
            parallel {
              
                stage('Main Branch ') {
                   
                    steps {
                          withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                      
                                  // Simulating some processing time
                            //sleep 5
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
