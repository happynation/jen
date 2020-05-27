pipeline {
    agent any

    stages {
        stage('ssh to ansible server') {
            steps {
                echo 'ssh ansible@192.168.1.96'
            }
        }
        stage('Check the syntax of playbook') {
            steps {
                echo 'sudo ansible-playbook /root/ansible_101/update.yaml --syntax-check'
            }
        }
        stage('Run playbook') {
            steps {
                echo 'sudo ansible-playbook /root/ansible_101/update.yaml -i /root/ansible_101/devhosts'
            }
        }
        
        }
    }
}
