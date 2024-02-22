/*buildPlugin(platforms: ['linux'],
        jdkVersions: [11,],
        checkstyle: [qualityGates: [[threshold: 1, type: 'NEW', unstable: true]]],
        pmd: [trendChartType: 'TOOLS_ONLY', qualityGates: [[threshold: 1, type: 'NEW', unstable: true]]])*/

node{
stage('git server'){
   echo "connecting to git server"
}
//stage('fetching the cyberark provided credentials'){
        //SSH ssh-privatekey-ID
  //withCredentials([conjurSecretUsernameSSHKey(credentialsId: 'ssh-git-username-cred', secretVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
     //sh 'echo $ssh-privatekey-ID | base64'
  //}
        //Git jenkins-git-credentials
 // withCredentials([gitUsernamePassword(credentialsId: 'ssh-privatekey-ID', gitToolName: 'Default')]) {
    //echo $jenkins-git-credentials
         // sh 'echo $ssh-privatekey-ID | base64'
//}
  // git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'

        //withCredentials([gitUsernamePassword(credentialsId: 'git-https-username-password', gitToolName: 'Default')]) {

               //test
               // sh 'echo $git-https-username-password | base64' 

        //}



        
  //}

   stage('Parallel Branches') {
            
             
                    steps {
                        script {

                     def parallelBranches = [:]

                        // Define parallel steps
                    parallelBranches['Step 1'] = {
                        withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                     echo "Executing Step 1 asynchronously"
                     sh 'echo $CONJUR_SECRET | base64'

                    }

                    }

                    parallelBranches['Step 2'] = {
                    withCredentials([conjurSecretCredential(credentialsId: 'test-pipeline-credential1', variable: 'CONJUR_SECRET')]) {
                     echo "Executing Step 2 asynchronously"
                     sh 'echo $CONJUR_SECRET | base64'

                    }

                    }
                           
                 
                        }     
                    
                }

   }
            
                // Add more stages for additional branches as needed
            
      


        
}
