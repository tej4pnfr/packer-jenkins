    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
          stage('Validate') {
            sh "echo hello"
             tool name: 'packer-jenkins', type: 'biz.neustar.jenkins.plugins.packer.PackerInstallation'
            sh "packer build web.json"
        }
    }
