node{
	stage('Checkout'){
		//Checkout the code from a GitHub repository
		git 'https://github.com/skeeto/sample-java-project.git'
	}
	stage('build'){
		sh '"/opt/maven/bin/mvn" -V clean compile'
	}
               stage('test'){
		sh '"/opt/maven/bin/mvn" -V clean test'
	}
	stage('package'){
		sh '"/opt/maven/bin/mvn" -V clean sonar:sonar'
	}
}
