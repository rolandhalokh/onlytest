def workspace
node {
   stage('Checkout') {
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '28a55c1b-a759-40d8-a6f6-bea6115087ab', url: 'git@github.com:rolandhalokh/onlytest.git']]])
       workspace = pwd()
   }
   stage('Static Code Analysis') {
       echo "Static Code Analysis step"
   }
   stage('Build') {
       echo "Build the code"
   }
   stage('Unit Testing') {
       echo "Unit testing step.."
   }
   stage('Delivery') {
       echo "Devivering the code"
   }
}
