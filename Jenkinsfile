pipeline {
    agent any
    stages {
        stage('Build on k8') {
            steps {
                bat 'xcopy helm\\* .'
                bat 'echo Current directory: %cd%'
                bat '"C:\\ProgramData\\chocolatey\\lib\\kubernetes-helm\\tools\\windows-amd64\\helm.exe" upgrade --install petclinic-app petclinic --set image.repository=registry.hub.docker.com/arunachaleswara369/petclinic --set image.tag=4'
            }
        }
    }
}
