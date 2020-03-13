    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
        stage('Build') {
            withCredentials([usernamePassword(credentialsId: '0c6365ff-1270-454c-91b6-a8ac76b07d1d', 'aws_access_keys', usernameVariable: 'AWS_ACCESS_KEY', passwordVariable: 'AWS_SECRET_KEY')]) {
            // Run the packer build
                sh "packer build  web.json"
           }
        }
        stage('Store Artifacts') {
            archiveArtifacts 'manifest.json'
        }
    }
