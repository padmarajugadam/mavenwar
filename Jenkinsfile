pipeline {
 agent any
options {
	buildDiscarder(logRotator(numToKeepStr: '2'))
}
	tools {
        maven 'maven' 
    }
	 stages {
    stage('Checkout external proj') {
        steps {
            git branch: 'developemtn',
                url: 'https://github.com/padmarajugadam/mavenwar.git'

            sh "ls -lat"
        }
    }
    stage('build') { 
	 steps {
             echo "build started" 
                sh 'mvn  clean install'
              
              echo "build completed"
            }
	 }
  stage('Approval') {
	  when { branch 'master' }
	  steps {
            input {
                message "Can we Proceed?"
                ok "Yes"
                submitter "Raju"
                parameters {
                    string(name: 'PERSON', defaultValue: 'DigiralVarys', description: 'Member')
                }
            }
            steps {
                echo "${PERSON}, is proceeding..."
            }
	  }
        }
      stage('deployment') { 
	 steps {
             echo "we will leran deployment" 
            
            }
	 }
		 stage('post') { 
	 steps {
             echo "post analysis" 
            
            }
	 }
}
}
