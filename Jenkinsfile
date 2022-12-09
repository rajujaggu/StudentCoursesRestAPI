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
                sh 'cd StudentCoursesRestAPI' 
                sh 'docker image build -t studentcoursestep1:1.0'
            }
        }
}

}