pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                sh 'sudo ansible -m ping all' 
            }
        }
        stage('Test'){
            steps {
                sh 'sudo ansible-playbook htmlapp.yml --syntax-check'
              
            }
        }
        stage('Deploy') {
            steps {
                sh 'sudo ansible-playbook htmlapp.yml'
            }
        }
    }
}
