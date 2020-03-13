    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
        stage('Validate') {
            sh "packer validate web.json"
            sh "echo $?"
        }
        stage('Build') {
            withCredentials([usernamePassword(credentialsId: '02ed7b09-4077-4d8d-a41a-eb7f2dc6d27a', 'aws_access_keys', usernameVariable: 'AWS_ACCESS_KEY', passwordVariable: 'AWS_SECRET_KEY')]) {
            // Run the packer build
                sh "packer build  web.json"
            }
        }
        stage('Store Artifacts') {
            archiveArtifacts 'manifest.json'
        }
    }
