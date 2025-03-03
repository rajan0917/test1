pipeline {
    agent any 
    stages {
        stage(name: 'Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/rajan0917/test1.git' 
            }
        }
        stage(name: 'Build Docker Image with Ansible') {
            steps {
                sh 'ansible-playbook -i inventory.yml build_docker.yml'
            }
        }
     }
}
