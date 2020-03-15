    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
        stage 'A'){
    tool name: 'packer-jenkins', type: 'biz.neustar.jenkins.plugins.packer.PackerInstallation' 
    sh ('packer-jenkins centos.json')
       }
  
          stage('Validate') {
            sh "echo hello     
                }
    }
