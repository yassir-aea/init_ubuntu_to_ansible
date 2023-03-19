
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh " print "DEBUG: parameter IP_ADDRESS = ${IP_ADDRESS}" >> hosts"    
                sh ''' #!/bin/bash
                 echo "hello world" 
                 echo 'P@ssword2020' | ansible-playbook ubuntu_init_with_ansible.yaml -i hosts -u root -k '''

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying.....'
            }
        }
    }
}
