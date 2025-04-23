pipeline {
 agent any
	tools {
        maven 'maven' 
    }
	 stages {
    stage('Analysis') {
	 steps {
            
                sh 'mvn  clean install'
              
              
            }
	 }
	 
}
}
    
