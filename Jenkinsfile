node {
   stage ('First Step') {
       echo 'Inside of First Step Stage!!!'
       stage('run-parallel-branches') {
           def stepsToRun = [:]
           for (int i = 1; i < 5; i++) {
             stepsToRun["Step${i}"] = { node {
                echo "start"
                sleep 5
                echo "done"
             }}
           }
       parallel stepsToRun
       }
       input 'Do you want to deploy?'  
   }
   stage('External library!') {
         echo "Testing if external library works!"
         def newUtils = new org.utils.myUtils()
         newUtils.echoStuff("Echoing the stuff inside my method!!!")
   }
}
