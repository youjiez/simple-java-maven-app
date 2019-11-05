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
            
            sh "export MAVEN_HOME=/root/Devops/apache-maven-3.6.2"       
            sh "export PATH=$MAVEN_HOME/bin:$PATH"            
            sh "mvn -Dmaven.test.failure.ignore=true clean package"

            // To run Maven on a Windows agent, use
            // bat "mvn -Dmaven.test.failure.ignore=true clean package"
         }

      }
   }
}
