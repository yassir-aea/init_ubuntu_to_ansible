
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                print "DEBUG: parameter IP_ADDRESS = ${IP_ADDRESS}"
                sh 
                sh ''' #!/bin/bash
                 echo "hello world" 
                 echo '@ssword2020' | ansible-playbook ubuntu_init_with_ansible.yaml -i hosts -u root -k '''
                sh 'mkdir test'
                sh 'rm -rf test'
                echo 'Building..'
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
