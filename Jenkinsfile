pipeline {
    agent any
    stages
    {
        stage('checkout from Git')
    {
        steps{
            echo "Checking out from git"
        
        }
    }
        
    stage('Building')
    {
        steps{
        echo 'This is the build stage'
        }
        
    }
    stage('At Jenkins')
    {
        steps{
            echo "At jenkins now"
        }
    }
    stage('AT s3')
    {
    steps{
   s3Upload(consoleLogLevel: 'INFO', dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'ns-jenkins-bucket', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: false, selectedRegion: 'us-east-1', showDirectlyInBrowser: false, sourceFile: 'jenkins_git_source_file.py', storageClass: 'STANDARD', uploadFromSlave: true, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 'ns-jenkins-bucket', userMetadata: [])
   }
    }
}
}
