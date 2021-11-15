pipeline {
	agent any
	stages{

		stage('clone and clean repo'){
			steps {
				cleanWs()
				sh "git clone -b master https://github.com/mohamedwassim817/MyAppWassim.git"
			}
		}
               stage('Build')
		{
			steps{
				script{
					sh "ansible-playbook MyAppWassim/ansible/build.yml -i MyAppWassim/ansible/inventory/host.yml"
				}
			}
		}
		

	}
}
