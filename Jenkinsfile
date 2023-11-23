node ('JDK8') {
	stage ('source code') {
		git branch: 'sprint1_develop', url: 'https://github.com/akkireddysandeep/game-of-life.git'
	}
	stage ('Buil the code') {
		sh 'mvn clean package'
	}
	stage ('Archiving and Test Results') {
		junit '**/surefire-reports/*xml'
		archiveArtifacts artifacts: '**/*.war', followSymlinks: false
	}
}

