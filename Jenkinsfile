    node {
        agent any
          tools {
        packer 'packer-jenkins' 
    }
        stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
        }
        stage ('A'){
         //sh "/var/jenkins_home/tools/biz.neustar.jenkins.plugins.packer.PackerInstallation/packer-jenkins/packer build /var/jenkins_home/workspace/packer-pipeline/web.json"
    //tool name: 'packer-jenkins', type: 'biz.neustar.jenkins.plugins.packer.PackerInstallation' 
    sh ('packer web.json')
       }
  
          stage('Validate') {
            sh "echo hello"   
                }
    }
