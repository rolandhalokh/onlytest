node {
   stage ('checkout SCM') {
        echo 'Get the code!!!!'
        git 'https://github.com/rolandhalokh/onlytest.git'
   }
   stage ('Test and Deploy') {
       echo 'Inside of Second Stage!!!'
       stage('run-parallel-branches') {
           def stepsToRun = [:]
           for (int i = 1; i < 5; i++) {
             stepsToRun["Step${i}"] = { node {
                echo "start"
                sleep 5
                echo "done"
             }}
           }
       }
       input 'Do you want to deploy?'  
   }
   stage('Deployment stage!') {
         echo "Lets DEPLOY!"
   }
}
