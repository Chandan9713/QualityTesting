node {
    
    
  /*  stage "Create build output"
    
     // Make the output directory.


    // Write an useful file, which is needed to be archived.
    writeFile file: "output/usefulfile.txt", text: "This file is useful, need to archive it."

    // Write an useless file, which is not needed to be archived.
    writeFile file: "output/uselessfile.md", text: "This file is useless, no need to archive it."


    stage "Archive build output"

    
    // Archive the build output artifacts.
    archiveArtifacts artifacts: 'output/*.txt', excludes: 'output/*.md'  */
     stage ('Stage Checkout')
    {

  // Checkout code from repository and update any submodules
  checkout scm
  bat 'git submodule update --init'  
    }


 stage ('Stage Build')
    {
  //branch name from Jenkins environment variables
  echo "My branch is: ${env.BRANCH_NAME}"

  def flavor = flavor(env.BRANCH_NAME)
  echo "Building flavor ${flavor}"

  //build your gradle flavor, passes the current build number as a parameter to gradle
  bat "./gradlew clean assemble${flavor}Debug -PBUILD_NUMBER=${env.BUILD_NUMBER}"
    }
}
 /* stage ('Stage Archive')
    {
  //tell Jenkins to archive the apks
  archiveArtifacts artifacts: 'app/build/outputs/apk/*.apk', fingerprint: true
    }
  stage ('Stage Upload To Fabric')
    {
  bat "./gradlew crashlyticsUploadDistribution${flavor}Debug  -PBUILD_NUMBER=${env.BUILD_NUMBER}"
}
}
// Pulls the android flavor out of the branch name the branch is prepended with /QA_
/*@NonCPS
def flavor(branchName) {
  def matcher = (env.BRANCH_NAME =~ /QA_([a-z_]+)/)
  assert matcher.matches()
  matcher[0][1]

   

}  */  

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
    }

    failure {
        mail(from: "cvsuccess2@gmail.com",
                to: "cvsuccess2@gmail.com",
                subject: "That build failed!",
                body: "Nothing to see here")
    }
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

