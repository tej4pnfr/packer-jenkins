    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
          stage('Validate') {
            sh '''
              "echo hello"
            "packer build web.json"
            '''
        }
    }
