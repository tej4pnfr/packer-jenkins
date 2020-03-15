    node {
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
        stage ('A'){
         sh "/var/jenkins_home/tools/biz.neustar.jenkins.plugins.packer.PackerInstallation/packer-jenkins/packer build /var/jenkins_home/workspace/packer-pipeline/centos.json"
    //tool name: 'packer-jenkins', type: 'biz.neustar.jenkins.plugins.packer.PackerInstallation' 
    //sh ('packer-jenkins centos.json')
       }
  
          stage('Validate') {
            sh "echo hello"   
                }
    }
