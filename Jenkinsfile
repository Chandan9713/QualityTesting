pipeline {
  agent any

  // This defines job parameters that are populated before job is run or default is used
  parameters {
    booleanParam(defaultValue: true, description: '', name: 'flag')
    string(defaultValue: '', description: '', name: 'SOME_STRING')
  }

  // Triggers define how the job is triggered.
  // Jobs may still be triggered manually or by webhook as well here.
  triggers {
    cron('@daily')
  }

  // Options covers all other job properties or wrapper functions that apply to entire Pipeline.
  options {
    buildDiscarder(logRotator(numToKeepStr:'1'))
    disableConcurrentBuilds()
    skipDefaultCheckout(true)
    timeout(time: 5, unit: 'MINUTES')
    timestamps()
  }

  stages {
    stage("foo") {
      steps {
        echo "hello"
        //bat 'test -f Jenkinsfile'
      }
    }
  }
}



/*
pipeline {
   agent any
   // triggers {
      //  cron('* * * * *')
   // }
   tools {
            // Here we have pairs of tool symbols (not all tools have symbols, so if you
            // try to use one from a plugin you've got installed and get an error and the
            // tool isn't listed in the possible values, open a JIRA against that tool!)
            // and installations configured in your Jenkins master's tools configuration.
            maven "apache-mavan"
          
        }

        environment {
            // Environment variable identifiers need to be both valid bash variable
            // identifiers and valid Groovy variable identifiers. If you use an invalid
            // identifier, you'll get an error at validation time.
            // Right now, you can't do more complicated Groovy expressions or nesting of
            // other env vars in environment variable values, but that will be possible
            // when https://issues.jenkins-ci.org/browse/JENKINS-41748 is merged and
            // released.
           mvnHome = 'c://apache-mavan'
       }

       stages {
            // At least one stage is required.
            stage("Preparation") {
                // Every stage must have a steps block containing at least one step.
               steps {
                    // Get some code from a GitHub repository
                    git 'https://github.com/Chandan9713/comProject2.git'
                }
          }
       }
        //   stage('Build') {
              //  steps {
                // Run the maven build
            //  if (isUnix()) {
               //     sh "'${mvnHome}/bin/mvn' clean test -Dtest=TestRunner"
              //  } else {
                    
                 // bat(/"${mvnHome}\bin\mvn" clean compile -Dtest=TestRunner/)
                  //  bat  "cd c:/Program Files/Jenkins/workspace/test-4"
                    //bat "mvn clean test C:/Program Files/Jenkins/workspace/test-4/pom.xml -Dtest=TestRunner"
               // }
           // }
           // }
       
           // stage('Results') {
           // steps {
            //    cucumber buildStatus: 'UNSTABLE', failedFeaturesNumber: 999, failedScenariosNumber: 999, failedStepsNumber: 3, fileIncludePattern: '.json', skippedStepsNumber: 999
          // }
         //   }
      // }
     //   }
     //   }
    
        // Post can be used both on individual stages and for the entire build.
    /*   post {
            
             success {
                echo 'Test run completed succesfully'
                 mail(from: "cvsuccess2@gmail.com",
                to: "cvsuccess2@gmail.com",
                subject: "That build passed.",
                body: "Nothing to see here")
            }
            failure {
                echo 'Test run failed'
                  mail(from: "cvsuccess2@gmail.com",
                to: "cvsuccess2@gmail.com",
                subject: "That build failed!",
                body: "Nothing to see here")
            }
           unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
            always {
        // Let's wipe out the workspace before we finish!
                deleteDir()
                echo "Workspace cleaned"
            }
    

  /* success {
        mail(from: "cvsuccess2@gmail.com",
                to: "cvsuccess2@gmail.com",
                subject: "That build passed.",
                body: "Nothing to see here")
   // }

    failure {
        mail(from: "cvsuccess2@gmail.com",
                to: "cvsuccess2@gmail.com",
                subject: "That build failed!",
                body: "Nothing to see here")
   // }
       }*/
      
    // The options directive is for configuration that applies to the whole job.
   /* options {
        // For example, we'd like to make sure we only keep 10 builds at a time, so
        // we don't fill up our storage!
        buildDiscarder(logRotator(numToKeepStr:'10'))

        // And we'd really like to be sure that this build doesn't hang forever, so
        // let's time it out after an hour.
        timeout(time: 60, unit: 'MINUTES')
    }
 
}*/

