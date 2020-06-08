#!groovy
@Library('piper-lib-os') _
node('BuildAgent-001') {
    stage('prepare') {
        deleteDir()
        checkout scm
        echo readYaml(text: "---")
      //  def data = readYaml file: 'mta.yaml'
        echo pwd
        setupCommonPipelineEnvironment script:this, runStageInPod: true
        //piperPipeline script: this, runStageInPod: true
        echo pwd
        sh "ls -ltr /ngs/app/sapopsd/jenkins-agent-home/workspace/Build-SCP-template-application/"

    }
    stage('build') {
        echo "-----------------------------------------------------------------"
        echo pwd
        sh "ls -la ${pwd()}"
        sh "ls -ltr /ngs/app/sapopsd/jenkins-agent-home/workspace/Build-SCP-template-application/"
        mtaBuild script: this, commonPipelineEnvironment.configuration.general.runStageInPod: true
    }
}
