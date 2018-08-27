node {
   stage ('checkout SCM') {
        echo 'Get the code!!!!'
        git 'https://github.com/rolandhalokh/onlytest.git'
   }
   stage ('Test and Deploy') {
       echo 'Inside of Second Stage!!!'
       stage('run-parallel-branches') {
         parallel(
           a: {
             echo "This is branch a"
           },
           b: {
             echo "This is branch b"
             sh './script.sh'
           }
         )
       }
       input 'Do you want to deploy?'  
   }
   stage('Deployment stage!') {
         echo "Lets DEPLOY!"
   }
}
