node {
   stage ('checkout SCM') {
        echo 'Get the code!!!!'
        git 'https://github.com/rolandhalokh/onlytest.git'
   }
   stage ('SecondStage') {
       echo 'Inside of Second Stage!!!'
       stage('run-parallel-branches') {
          echo "This is branch a"
          echo "This is branch b"
          sh "script.sh"
        }
   }
}
