@Library(value="utilities-portal-library@master", changelog=false)
import org.utils.myUtils

node {
   stage ('First Stage') {
       echo 'Inside of First Stage!!!'
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
   stage('Test Library Stage') {
         echo "Testing if external library works!"
         def newUtils = new org.utils.myUtils()
         newUtils.echoStuff("Echoing the stuff inside my method!!!")
   }
}
