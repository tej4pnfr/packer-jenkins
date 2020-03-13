    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
          stage('Validate') {
            sh "echo hello"
            sh "ansible-playbook web.yml --syntax-check"
        }
    }
