pipeline{
    agent any
    stages{
        stage('SCM checkout')
        {
          
            steps{
                git 'https://github.com/chpadmavathi/DevOps-Project.git'
            }
        }
        stage('Ansible playbook')
        {
            steps{
                ansiblePlaybook credentialsId: 'myansible', disableHostKeyChecking: true, installation: 'myansible', inventory: 'dev.inv', playbook: 'playbook1.yml'
            }
        }
    }
}
