pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

                sh '''#!/bin/bash
                 echo "hello world" 
                 echo '@ssword2020' | ansible-playbook ubuntu_init_with_ansible.yaml -i hosts -u root -k
         '''
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
}
