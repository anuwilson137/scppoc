#!groovy
@Library('piper-lib-os') _
node('BuildAgent-001') {
    stage('prepare') {
        deleteDir()
        checkout scm
        echo readYaml(text: "---")
      //  def data = readYaml file: 'mta.yaml'
        echo pwd
        setupCommonPipelineEnvironment script:this
        piperPipeline script: this, runStageInPod: false
        mtaBuild script: this
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
