pipeline {
    agent any
     environment {
    PACKER_HOME = tool name: 'packer-jenkins', type: 'biz.neustar.jenkins.plugins.packer.PackerInstallation'
}   
    stages {
        stage('Example') {
            steps {
                sh '$PACKER_HOME/packer --version'
                sh '$PACKER_HOME/packer validate web.json'
                sh '$PACKER_HOME/packer build web.json'
            }
        }
    }
}
