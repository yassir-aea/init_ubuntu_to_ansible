
pipeline {
    agent {
       label "${ubuntu-agent}"
    }
    
    stages {
        stage('Build') {
            steps {
                
                print "DEBUG: parameter IP_ADDRESS = ${IP_ADDRESS}"
                sh 'echo $IP_ADDRESS >> hosts'  
                sh ' cat hosts'
                sh 'echo ${IP_ADDRESS} '
                sh ''' #!/bin/bash
                 echo "hello world"                  
                 echo 'P@ssword2020' | ansible-playbook ubuntu_init_with_ansible.yaml -i hosts -u root '''

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
