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
        sh "ls -la ${pwd()}"
    }
    stage('build') {
        echo "-----------------------------------------------------------------"
        echo pwd
        sh "ls -la ${pwd()}"
        mtaBuild script: this
    }
}
