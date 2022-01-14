def pipelineContext = [:]
node{
stage('Clone') {
git 'https://github.com/kabsty/app-salaire.git'
}
stage('Ansible') {
ansiblePlaybook (
colorized: true,
become: true,
playbook: 'installation.yaml',
inventory: 'hosts.yaml'
)
}
}
