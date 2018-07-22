node {
    stage('SCM') {
        git 'https://github.com/wakaleo/game-of-life.git'
    }
    
    stage('Build ') {
        sh 'mvn install'
    }
    stage('Archiving the Artifacts') {
        archiveArtifacts 'gameoflife-web/target/gameoflife.war'
    }
    stage('Publishing Junit'){
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}