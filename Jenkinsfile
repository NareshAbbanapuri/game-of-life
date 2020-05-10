node('build') {
    stage('scm') {
    git 'https://github.com/wakaleo/game-of-life.git'
}
stage('build') {
    sh label: '', script: 'mvn package'
}
 stage('Junit'){
     junit 'gameoflife-web/target/surefire-reports/*.xml'
 }
 stage('artifact'){
     archive 'junit \'/gameoflife-web/target/*.war'
 }
}
