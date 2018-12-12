# Docker: env-show

Docker example: my very simple container.


## Container:

    env | sort | awk -F= '{printf "%10s=%s\n", $1, $2}'


Shows container's environment variables at runtime.


## Tasks:

    make vars  - Defined vars for [env-show]

    make build - Run 'docker build'
    make img   - Run 'docker images' for [env-show]
    make imgs  - Run 'docker images' for all
    make tag   - Run 'docker tag' latest to [v0]
    make tags  - Run 'docker tag' latest to ECR and DockerHub

    make run   - Run 'docker run -t -i env-show'
    make sh    - Run 'docker run -t -i env-show /bin/sh'
    make bash  - Run 'docker run -t -i env-show /bin/bash'

    make ecr   - Run 'docker push' to ECR: [aws-account-id.dkr.ecr.region.amazonaws.com:env-show]
    make hub   - Run 'docker push' to DockerHub: [repo/env-show]

    make clean_imgs - Cleanup: remove local [env-show] images
    make clean_tags - Cleanup: remove REMOTE tags
    make clean      - Cleanup: remove local images and REMOTE tags

    make ecr_create - ECR: Create repo for [env-show]
    make ecr_login  - ECR: Login

    make ver      - Current version: [env-show:v0]
    make upver    - Current version + 1
    make resetver - Reset version to [v0]


