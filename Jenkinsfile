def workspace
node
{
    stage ( 'wordpressclone')
    {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '52a7af3e-db98-47c2-af29-1fd4b239df04', url: 'https://github.com/thakurpractise/learnings.git']]])
        workspace = pwd ()
    }
    stage ('wordpressdeployment')
    {
        build job: 'wordpressdeployment', parameters: [string(name: 'workspace', value: 'workspace')]
        workspace = pwd ()
    }
    stage ('wordpressdbcreation')
    {
        build job: 'wordpressdbcreation', parameters: [string(name: 'workspace', value: 'workspace')]
        workspace = pwd ()
    }
}
