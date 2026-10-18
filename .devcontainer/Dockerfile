FROM mcr.microsoft.com/devcontainers/base:debian

# Max Server-Side SSH Optimization
RUN sudo sed -i 's/#UseDNS yes/UseDNS no/; s/UseDNS yes/UseDNS no/' /etc/ssh/sshd_config && \
    sudo sed -i 's/#GSSAPIAuthentication yes/GSSAPIAuthentication no/; s/GSSAPIAuthentication yes/GSSAPIAuthentication no/' /etc/ssh/sshd_config && \
    echo "Ciphers chacha20-poly1305@openssh.com,aes256-gcm@openssh.com" | sudo tee -a /etc/ssh/sshd_config && \
    echo "KexAlgorithms curve25519-sha256@libssh.org,diffie-hellman-group-exchange-sha256" | sudo tee -a /etc/ssh/sshd_config