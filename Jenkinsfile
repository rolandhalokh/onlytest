@Library(value="library@master", changelog=false) _
import org.conf.*

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

         //Employee employee = new Employee(firstName:"John", lastName:"Doe", salary:"20000")
         //println(employee.firstName)
         //println(employee.lastName)
         //println(employee.salary)
   }
}
