    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        } 
       stage('Store Artifacts') {
            archiveArtifacts 'manifest.json'
        }
    }
