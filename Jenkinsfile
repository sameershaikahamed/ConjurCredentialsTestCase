/*pipeline {
    agent any

    //triggers {
        // Use to trigger the pipeline every minute
      //  pollSCM('* * * * *')
   // }

    stages {
        stage('conjur-credentials Main Branch') {
            steps {
                withCredentials([conjurSecretCredential(credentialsId: 'test-multibranch-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                 //withCredentials([gitUsernamePassword(credentialsId: 'test-multibranch-pipeline-credential1', gitToolName: 'Default')]) {
                   //withCredentials([conjurSecretCredential(credentialsId: 'test-multibranch-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                  //withCredentials([conjurSecretUsername(credentialsId: 'test-multibranch-pipeline-credential1', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'sameer.shaik@cyberark')]) {
 
                   sh ' echo $CONJUR_SECRET | base64'
                
                }
            }
        }
    }
}*/

buildPlugin(platforms: ['linux'],
        jdkVersions: [11,],
        checkstyle: [qualityGates: [[threshold: 1, type: 'NEW', unstable: true]]],
        pmd: [trendChartType: 'TOOLS_ONLY', qualityGates: [[threshold: 1, type: 'NEW', unstable: true]]])
