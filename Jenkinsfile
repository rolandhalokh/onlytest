@Library(value="utilities-portal-library@master", changelog=false)
import org.conf.buildUtils.*

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

         def podname = org.demo.generatePodname("salala")
         echo "${podname}"
   }
}
