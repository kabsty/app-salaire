def pipelineContext = [:]
node{
    stage('Clone') {
        git 'https://github.com/kabsty/app-salaire.git'
    }

    stage('Ansible'){
       sh '''
       ansible-playbook start_project.yaml -i hosts
       '''
    }
}    


