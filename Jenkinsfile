pipeline {
 agent any
	tools {
        maven 'mzven' 
    }
	 stages {
    stage('build') {
	 steps {
             echo "build started" 
                sh 'mvn  clean install'
              
              echo "build completed"
            }
	 }

}
}
    
