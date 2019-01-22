FROM openshift/jenkins-slave-base-centos7:latest

RUN yum groupinstall 'Development Tools' -y && yum install wget -y \
    mkdir /go

ENV GOLANG_VERSION 1.11.4
ENV KUBEBUILDER_VERSION 1.0.7
RUN set -eux; \
	\
	url="https://golang.org/dl/go${GOLANG_VERSION}.linux-amd64.tar.gz"; \
	wget -O go.tgz "$url"; \
	echo "fb26c30e6a04ad937bbc657a1b5bba92f80096af1e8ee6da6430c045a8db3a5b *go.tgz" | sha256sum -c -; \
	tar -C /usr/local -xzf go.tgz; \
	rm go.tgz; \
  kubebuilderurl="https://github.com/kubernetes-sigs/kubebuilder/releases/download/v${KUBEBUILDER_VERSION}/kubebuilder_${KUBEBUILDER_VERSION}_linux_amd64.tar.gz" ;\
  wget -O kubebuilder.tar.gz "$kubebuilderurl";\
  tar zxvf kubebuilder.tar.gz ;\
  mv kubebuilder_${KUBEBUILDER_VERSION}_linux_amd64 /usr/local/kubebuilder ;\
	export PATH="/usr/local/kubebuilder/bin:/usr/local/go/bin:$PATH"; \
	go version

ENV GOROOT /usr/local/go
ENV GOPATH /go
ENV PATH $GOPATH/bin:$GOROOT/bin:$PATH
