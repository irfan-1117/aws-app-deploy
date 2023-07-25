pipeline {
    agent any

    environment {
        EC2_INSTANCE_IP = '44.198.52.159'
        SSH_PRIVATE_KEY = credentials('SSH-KEY')
    }

    tools {
     dockerTool 'Docker'
    }
 
    stages {
        stage('Clean workspace') {
            steps {
              cleanWs()
            }
        }

        /*stage('Checkout-SCM') {
            steps {
               git branch: 'development', url: 'https://github.com/irfan-1117/aws-app-deploy.git'
            }
        }*/

        stage('Deploy to EC2') {
            steps {
                script {
                    // SSH agent is now active, you can run SSH commands here
                    sh "ssh -o StrictHostKeyChecking=no -i $SSH_PRIVATE_KEY ubuntu@$EC2_INSTANCE_IP"
                }    
            }
        }
    }
} 