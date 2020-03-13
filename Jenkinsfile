    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
        stage('Validate') {
            sh "packer validate jenkins.json"
            sh "ansible-playbook jenkins.yml --syntax-check"
        }
        stage('Build') {
      withCredentials([usernamePassword(credentialsId: '02ed7b09-4077-4d8d-a41a-eb7f2dc6d27a', passwordVariable: 'AWS_SECRET', usernameVariable: 'AWS_KEY')
            // Run the packer build
		{
                sh "packer build jenkins.json"
            }
        }
        stage('Store Artifacts') {
            archiveArtifacts 'manifest.json'
        }
    }
