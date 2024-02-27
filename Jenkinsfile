node {
  stage('========== Clone repository ==========') {
    checkout scm
  }
  stage('========== Build image ==========') {
    echo "Build image"
  }
  stage('========== docker login ==========') {
	steps { 
	  script {
		sh 'docker login 192.168.10.68'
	  } 
	}	
  }  
  stage('========== Push image ==========') {
    echo "Build image"
  }
}
