node {
   stage ('First Step') {
       echo 'Inside of First Step Stage!!!'
       stage('run-parallel-branches') {
           def stepsToRun = [:]
           for (int i = 1; i < 3; i++) {
             stepsToRun["Step${i}"] = { node {
                echo "start"
                echo "done"
             }}
           }
       parallel stepsToRun
       } 
   }
   stage('External library!') {
        // echo "Testing if external library works!"
        // def newUtils = new org.utils.myUtils()
        // newUtils.echoStuff("Echoing the stuff inside my method!!!")
   }
}
