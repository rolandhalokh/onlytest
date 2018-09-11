@Library('utilities-portal-library/master')_
import org.utils.*

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
         def newUtil = new org.utils.myUtils()
         newUtil.echoStuff("Echoing the stuff inside my method!!!")
   }
}
