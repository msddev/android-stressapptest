Run on Linux:

sudo -s

apt install g++ gawk git make

git clone https://github.com/stressapptest/stressapptest.git

cd stressapptest

./configure

make install

stressapptest

stressapptest -M 25300

stressapptest -M 25300 -s 3600






Run on Android:

cd /Users/snapp/stressapp/stressapptest/libs/arm64-v8a

adb push stressapptest /data/local/tmp/
adb shell chmod 777 /data/local/tmp/stressapptest
adb shell /data/local/tmp/stressapptest -M 2500 -s 20

adb devices
adb -s emulator-5556 shell /data/local/tmp/stressapptest
