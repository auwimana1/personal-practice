pipeline{
    agent any

    parameters{
        (name: 'Adelina' , defaultValue: '1.0.0')
    }


    stages{
        stage("build image and push to ecr"){
            steps{
                script{
                    // This step should not normally be used in your script. Consult the inline help for details.
                withDockerRegistry(credentialsId: 'ecr:us-east-1:Adelina_IAM', url: 'https://ec2-54-85-165-221.compute-1.amazonaws.com/') {
                sh "docker build -t my-practice ."
                sh "docker tag my-practice:latest 557195342730.dkr.ecr.us-east-1.amazonaws.com/my-practice:latest"
                sh "docker tag my-practice:latest 557195342730.dkr.ecr.us-east-1.amazonaws.com/my-practice:latest"
                sh "docker push 557195342730.dkr.ecr.us-east-1.amazonaws.com/my-practice:latest"
                sh "docker push 557195342730.dkr.ecr.us-east-1.amazonaws.com/my-practice:latest" 
}
                }
            }
        }
        
     }
 }
    