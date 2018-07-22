node {
    stage('SCM') {
        git 'https://github.com/itzpraveen18/game-of-life.git'
    }
    
    stage('Build ') {
        sh 'mvn install'
		input message:'doing the Build pipe line '
    }
    stage('Archiving the Artifacts') {
        archiveArtifacts 'gameoflife-web/target/gameoflife.war'
    }
    stage('Publishing Junit'){
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}