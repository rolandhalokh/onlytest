node {
   stage ('checkout SCM') {
        echo 'Get the code!!!!'
        git 'https://github.com/brentlaster/gradle-greetings.git'
   }
   stage ('SecondStage') {
       echo 'Inside of Second Stage!!!'
       stage('run-parallel-branches') {
          steps {
            parallel(
              a: {
                echo "This is branch a"
              },
              b: {
                echo "This is branch b"
              }
            )
          }
      }
   }
}
