/*node {
    
    
    stage "Create build output"
    
    
    // Make the output directory.


    // Write an useful file, which is needed to be archived.
    writeFile file: "output/usefulfile.txt", text: "This file is useful, need to archive it."

    // Write an useless file, which is not needed to be archived.
    writeFile file: "output/uselessfile.md", text: "This file is useless, no need to archive it."


    stage "Archive build output"

    
    // Archive the build output artifacts.
    archiveArtifacts artifacts: 'output/*.txt', excludes: 'output/*.md'  
    
   
}*/

pipeline {
    agent any
    stages {
        stage("Verify")
        {    steps {
            fileExists 'C:\\Program Files\\Jenkins\\workspace\\test-41'
            
        }
    }
}
post {
    success
    {
        echo 'file exist in workspace'
    }
    failure
    {
        echo 'file doesnt exist in workspace'
    }
}
}
