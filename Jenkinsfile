pipeline {
    agent any 
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/rajan0917/test1.git' 
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    sh "chmod +x -R ${env.WORKSPACE}"
                    inventory: 'inventory',
                    playbook: 'ping.yaml',
                    installation: "ansible-playbook"
                    
                ) 
            }
        }
    }
    
    }
