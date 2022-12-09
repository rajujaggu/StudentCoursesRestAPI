pipeline{
    agent {label 'Docker'}
     triggers { 
        pollSCM('* * * * *') 
        }
     stages {
        stage ('vcs')
        {
            steps{
              git url: 'https://github.com/rajujaggu/StudentCoursesRestAPI.git',
                  branch: 'master'
            }
        }
        stage ('imagebuild'){
            steps{ 
                sh "docker image build -t studentcoursestep1:1.0 ."
                sh "docker image tag studentcoursestep1:1.0 rajreddy999"
                sh "docker image push rajreddy999"
            }
        }
}

}