pipeline {
 agent any
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
