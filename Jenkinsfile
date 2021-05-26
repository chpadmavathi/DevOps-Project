pipeline{
    agent any
    stages{
        stage('SCM checkout')
        {
          
            steps{
                git branch: 'main', url: 'https://github.com/chpadmavathi/DevOps-Project'
            }
        }
        stage('Ansible playbook')
        {
            steps{
                ansiblePlaybook credentialsId: 'private-key1', disableHostKeyChecking: true, installation: 'myansible', inventory: 'dev.inv', playbook: 'playbook1.yml'
            }
        }
    }
}
