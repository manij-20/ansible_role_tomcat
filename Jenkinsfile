pipeline {
    agent any

    stages {
        stage('Checkout Ansible Code') {
            steps {
                git branch: 'main', url: 'https://github.com/patilsahana1234/ansible_role_tomcat.git'
            }
        }

        stage('Deploy Tomcat using Ansible Role') {
            steps {
                sh '''
                  cd ansible_role_tomcat || exit 1
                  ansible-playbook -i hosts.ini install_tomcat.yml
                '''
            }
        }
    }
}
