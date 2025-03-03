pipeline {
    agent any 
     environment {
        PATH = "/usr/bin/ansible:/usr/bin/ansible-playbook:$PATH"
       
     }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/rajan0917/test1.git' 
            }
        }
        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    
                    inventory: 'inventory',
                    playbook: 'ping.yaml',
                    installation: "ansible-playbook"
                    
                ) 
            }
        }
    }
    
    }
