# Anbox-on-TW
Install Anbox on openSUSE Tumbleweed without using snap
How to install Anbox without snap in TW

1. install  kernel-default , anbox , properties-cpp from repo https://build.opensuse.org/project/show/home:munix9:test

2 . Load some kernel modules  sudo modprobe ashmem_linux && sudo  modprobe binder_linux

3. download latest android image from https://build.anbox.io/android-images/ and put it as  /var/lib/anbox/android.img . 

4. After that systemctl enable --now anbox-container-manager.service and then  systemctl --user enable --now anbox-session-manager.service .

5. start anbox from the terminal using  anbox launch --package=org.anbox.appmgr --component=org.anbox.appmgr.AppViewActivity .

Thanks  : Arch wiki and @andres_bs of openSUSE Telegram channel for pointing out munix9's obs repo . 🙂
