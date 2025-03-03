pipeline {
    agent any 
    stages {
        stage(name: 'Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/rajan0917/test1.git' 
            }
        }
        stage(name: 'Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    
                    inventory: 'inventory',
                    playbook: 'ping.yaml', 
                    
                ) 
            }
        }
    }
