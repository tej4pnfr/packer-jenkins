node {
     agent any
     environment {
    PACKER_HOME = tool name: 'packer-jenkins', type: 'biz.neustar.jenkins.plugins.packer.PackerInstallation'       
      }
     stage('Checkout') {
            // Get some code from a GitHub repository
            checkout scm
      }

stage ('foo') {
  sh("${PACKER_HOME}/packer --version")
}
  stage ('A'){
         //sh "/var/jenkins_home/tools/biz.neustar.jenkins.plugins.packer.PackerInstallation/packer-jenkins/packer build /var/jenkins_home/workspace/packer-pipeline/web.json"
    //tool name: 'packer-jenkins', type: 'biz.neustar.jenkins.plugins.packer.PackerInstallation' 
    sh 'packer web.json'
      }
  
       //   stage('Validate') {
         //   sh "echo hello"   
          //      }
    }
