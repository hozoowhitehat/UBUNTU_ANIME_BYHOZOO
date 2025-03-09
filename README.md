# UBUNTU_ANIME_BYHOZOO
💻📱

git clone https://github.com/hozoowhitehat/UBUNTU_ANIME_BYHOZOO



cd UBUNTU_ANIME_BYHOZOO

sudo docker run --rm \
  --interactive \
  --tty \
  --volume "$PULSE_PATH:/run/user/1000/pulse/native" \
  --privileged \
  --publish 6080:6080 \
  --publish "$VNC_PORT:5900" \
  --publish "$SSH_PORT:22" \
  --name desktop \
  --env DESKTOP_ENV=xfce4 \
  --env LANG=fr_FR.UTF-8 \
  --env DESKTOP_KEYBOARD_LAYOUT="fr/azerty" \
  --env DESKTOP_SIZE="1920x1080" \
  --env DESKTOP_THEME="Greybird-dark" \
  --env DESKTOP_BACKGROUND_IMAGE="https://i.ibb.co/bjvyS5z/anime-anime-girls-sword-red-fan-art-hd-wallpaper-preview.jpg" \
  --env USR_UID="$(id -u)" \
  --env USR_GID="$(id -g)" \
  docker-vnc-xfce4 /bin/bash
  
