// Pushing DOCKER image to ECR.


pipeline {
  agent any
  environment {
    AWS_ACCOUNT_ID = "381492106362"
    AWS_DEFAULT_REGION = "ap-south-1"
    IMAGE_REPO_NAME = "docker-image"
    IMAGE_TAG = "1.0"
    REPOSITORY_URI = "${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}"
  }

  stages {

    stage('Logging into AWS ECR') {
      steps {
        script {
          sh "aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 381492106362.dkr.ecr.ap-south-1.amazonaws.com"
        }

      }
    }



    // Building Docker images
    stage('Building image') {
      steps {
        script {
          sh "docker image build -t httpd:1.0 ."
        }
      }
    }

    // Uploading Docker images into AWS ECR
    stage('Pushing to ECR') {
      steps {
        script {
          sh "docker tag httpd:1.0 ${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}/httpd:${IMAGE_TAG} "
          sh "docker push ${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}:${IMAGE_TAG}"
        }
      }
    }
  }
}