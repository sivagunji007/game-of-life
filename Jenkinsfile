node('ltecomm') {
    stage('scm') {
        git 'https://github.com/shaikkhajaibrahim/game-of-life.git'
    }

    stage('build'){
        sh label: '', scrpit: 'mvn clean package'

    }
    
    stage('postbuild'){
        junit 'gameoflife-web/target/surefire-reports/*.xml'
        archiveArtifacts 'gameoflife-web/target/*.war'    
    }
 
}