node {
    stage "Create build output"
    
    // Make the output directory.
    sh "mkdir -p "e:/output"

    // Write an useful file, which is needed to be archived.
    writeFile file: "e:/output/usefulfile.txt", text: "This file is useful, need to archive it."

    // Write an useless file, which is not needed to be archived.
    writeFile file: "e:/output/uselessfile.md", text: "This file is useless, no need to archive it."

    stage "Archive build output"
    
    // Archive the build output artifacts.
    archiveArtifacts artifacts: 'e:/output/*.txt', excludes: 'e:/output/*.md'
}
