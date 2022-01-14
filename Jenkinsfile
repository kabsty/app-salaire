def pipelineContext = [:]
node{
 stage('Clone') {
   git 'https://github.com/kabsty/app-salaire.git'
 }
 stage('Ansible') {
    ansiblePlaybook (
    colorized: true, 
    become: true, 
    playbook: 'install.yaml',
    inventory: 'hosts',
    credentialsId: 'fa847de9-9d9e-49b2-bee5-f88f17260161',
    disableHostKeyChecking: true
    )
  }
}

