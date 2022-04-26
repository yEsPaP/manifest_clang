# manifest_clang

to init:

`repo init -u https://github.com/yEsPaP/manifest_clang -b master -m manifest_4691093.xml`

sync:
`repo sync -c -j$(nproc --all) --no-tags --no-clone-bundle --optimized-fetch --prune`

build:

`python toolchain/llvm_android/build.py --no-build=linux`

fix possible missing header error:

`ln -s /usr/include/locale.h /usr/include/xlocale.h`
