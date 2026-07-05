FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04

# Instala GNOME completo + pacotes do Zorin
RUN apt-get update && apt-get install -y \
    ubuntu-desktop \
    gnome-session \
    gnome-shell \
    gnome-tweaks \
    zorin-os-themes \
    zorin-appearance \
    zorin-os-desktop \
    gnome-menus \
    nautilus \
    firefox \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Configurações extras para desktop no container
ENV DEBIAN_FRONTEND=noninteractive
RUN echo "exec gnome-session" > /etc/X11/Xsession.d/99-gnome-session

USER vscode
