@Library('library')_
//import org.conf.*
//library 'library'

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

         //imakeit 'Roland'

         def myUtils = new org.conf.buildUtils()
         myUtils.showIt 'Welcome home!!'
         

   }
}
