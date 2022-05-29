FROM fedora

# Setting up package manager
RUN echo max_parallel_downloads=10 >> /etc/dnf/dnf.conf
RUN echo fastestmirror=True >> /etc/dnf/dnf.conf

# Installing packages from package manager
RUN dnf upgrade -y
RUN dnf install -y git gcc cmake

# Installing Rust toolchain
RUN cd /root
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs -o rustup-installer
RUN chmod +x rustup-installer
RUN ./rustup-installer -y