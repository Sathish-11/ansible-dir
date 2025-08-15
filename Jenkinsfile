pipeline {
    agent any

    stages {
        stage('Git_Clone') {
            steps {
                git 'https://github.com/Sathish-11/ansible-dir.git'
                echo 'Git repo Cloned'
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook credentialsId: 'ansible-ssh', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'inventory.ini', playbook: 'install_apache.yml', vaultTmpPath: ''
            }
        }
    }
}
