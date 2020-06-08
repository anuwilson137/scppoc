#!groovy
library "piper-lib-os@always-spawn-pod"
@Library('piper-lib-os') _
node('BuildAgent-001') {
    stage('prepare') {
        deleteDir()
        checkout scm
        echo readYaml(text: "---")
      //  def data = readYaml file: 'mta.yaml'
        echo pwd
        script { 
    commonPipelineEnvironment.configuration.general.runStageInPod = true
}
        //setupCommonPipelineEnvironment script:this, runStageInPod: true
        //piperPipeline script: this, runStageInPod: true
        echo pwd
        sh "ls"
    }
    stage('build') {
        echo "-----------------------------------------------------------------"
        echo pwd
        sh "ls"
        mtaBuild script: this
    }
}
