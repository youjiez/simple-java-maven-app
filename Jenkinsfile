pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      maven "MAVEN3"
   }

   stages {
      stage('Build') {
         steps {
           

            // Run Maven on a Unix agent.
            
                  
            sh "mvn -B -DskipTests clean package"

            // To run Maven on a Windows agent, use
            // bat "mvn -Dmaven.test.failure.ignore=true clean package"
         }

      }
   }
}
