    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
          stage('Validate') {
            sh "echo hello"
            sh "packer-jenkins build web.json"
        }
    }
