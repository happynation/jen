pipeline {
    agent any

    stages {
        stage('ssh to ansible server') {
            steps {
                echo 'ssh ansible@192.168.1.96'
            }
        }
        stage('Check the version of Ansible') {
            steps {
                script {
                    version = 'ansible 2.9.8'
                }
                sh '''
                if [[ $(ansible --version | head -n 1) = $version ]]; then
                  exit 0
                else
                  exit 1
                fi
                '''
            }
        }
    }
}
