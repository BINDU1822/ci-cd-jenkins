// pipeline {
//     agent any
    
//     environment {
//         SONAR_SCANNER_HOME = tool name: 'SonarScanner', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
//     }
    
//     stages {
//         stage('Checkout') {
//             steps {
//                 // Checkout your Python code repository here (e.g., using Git)
//                 checkout scm
//             }
//         }
        
//         stage('Static Code Analysis') {
//             steps {
//                 // Install Python dependencies (e.g., using pip)
//                 sh 'pip install -r requirements.txt'
                
//                 // Run SonarScanner for Python
//                 sh "${SONAR_SCANNER_HOME}/bin/sonar-scanner"
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



// node{
//     stage('Cloning the project'){
//         // git 'https://github.com/BINDU1822/ci-cd-jenkins.git'
//       checkout scm
//     }
//     stage('Sonarqube Static code analysis'){
//         def scannerHome = tool 'sonarqube';
//         withSonarQubeEnv('sonarqube'){
//             sh "${scannerHome}/bin/sonar-scanner \
//             -D sonar.login=admin \
//             -D sonar.password=binduramesh@1822 \
//             -D sonar.projectkey=sonartest \
//             -D sonar.host.url=http://117.208.152.165:9000/"
//         }
//     }
// }
