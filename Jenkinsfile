node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t mockexam:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'fridahmanyaki' -p 'j3nk1ns' "
sh "docker tag mockexam:latest fridahmanyaki/mockexam:latest"
sh "docker push fridahmanyaki/mockexam:latest:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
