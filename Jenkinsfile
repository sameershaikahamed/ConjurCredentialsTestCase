/*buildPlugin(platforms: ['linux'],
        jdkVersions: [11,],
        checkstyle: [qualityGates: [[threshold: 1, type: 'NEW', unstable: true]]],
        pmd: [trendChartType: 'TOOLS_ONLY', qualityGates: [[threshold: 1, type: 'NEW', unstable: true]]])*/

node{
stage('git server'){
   echo "connecting to git server"
}
stage('fetching the cyberark provided credentials'){
  withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET_1')]) {
    echo $CONJUR_SECRET_1
}
  // git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
  }
}
