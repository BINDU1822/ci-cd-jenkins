// pipeline {
//     agent any
//     stages {
//         stage('Checkout') {
//             steps {
//                 checkout scm
//             }
//         }
        
//         stage('Static Code Analysis') {
//             steps {
//                 def scannerHome = tool 'sonarqube';
//                 withSonarQubeEnv('sonarqube'){
//                     sh 'pip install -r requirements.txt'
//                     sh "${scannerHome}/bin/sonar-scanner \
//                     -D sonar.login=admin \
//                     -D sonar.password=binduramesh@1822 \
//                     -D sonar.projectkey=sonartest \
//                     -D sonar.host.url=http://117.208.152.165:9000/"
                
//                 }
//             }
//         }
//     }
    
//     post {
//         always {
//             // Publish SonarQube results (optional)
//             // You can use the SonarQube Scanner for Jenkins plugin to publish the analysis results.
//         }
//     }
// }



node{
    stage('Cloning the project'){
        // git 'https://github.com/BINDU1822/ci-cd-jenkins.git'
      checkout scm
    }
    stage('Sonarqube Static code analysis'){
        def scannerHome = tool 'sonarqube';
        withSonarQubeEnv('sonarqube'){
            sh 'pip install -r requirements.txt'
            sh "${scannerHome}/bin/sonar-scanner \
            -D sonar.login=admin \
            -D sonar.password=binduramesh@1822 \
            -D sonar.projectkey=sonartest \
            -D sonar.exclusions=vendors/**,resources/**,**/*,java \
            -D sonar.host.url=http://117.208.152.165:9000/"
        }
    }
}
