ARG terraform_version=0.13.4

FROM hashicorp/terraform:$terraform AS terraform

FROM golang:1.15
RUN mkdir -p /.cache && chmod -R 777 /.cache
COPY --from=terraform /bin/terraform /bin/terraform
RUN go get -u golang.org/x/tools/gopls \
  && rm -rf /.cache/*
RUN apt update && apt install -y zip \
  && wget https://releases.hashicorp.com/terraform-ls/0.10.0/terraform-ls_0.10.0_linux_amd64.zip \
  && unzip terraform-ls_0.10.0_linux_amd64.zip \
  && rm terraform-ls_0.10.0_linux_amd64.zip \
  && mv terraform-ls /usr/bin
