__Instructions__

# First time only
git clone git@github.com:SickChill/qnap-chroot.git
cd qnap-chroot
# Every time except first time
git pull
git submodule update --init --recursive

# First time only
mkdir dev
mknod dev/null c 1 3

# Build it
sudo chroot .
/build-pkg.sh

# qpkg's are in the sickchill/build dir
