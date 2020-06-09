#!groovy
//node('BuildAgent-001') {
    @Library('piper-lib-os') _
    stage('prepare') {
        nodeLabel: 'BuildAgent-001'
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
        nodeLabel: 'BuildAgent-001'
        echo "-----------------------------------------------------------------"
        echo pwd
        sh "ls -la ${pwd()}"
        sh "ls -ltr /ngs/app/sapopsd/jenkins-agent-home/workspace/Build-SCP-template-application/"
        mtaBuild script: this
    }
}

