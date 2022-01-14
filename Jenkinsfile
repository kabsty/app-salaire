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
    credentialsId: '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',
    disableHostKeyChecking: true
    )
  }
}

