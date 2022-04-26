# manifest_clang

to init:

`repo init -u https://github.com/yEsPaP/manifest_clang -b master -m manifest_4691093.xml`

sync:
`repo sync -c -j$(nproc --all) --no-tags --no-clone-bundle --optimized-fetch --prune`

build:

`python toolchain/llvm_android/build.py`

fix possible missing header error:

`ln -s /usr/include/locale.h /usr/include/xlocale.h`,
https://reviews.llvm.org/rG383fe5c8668f63ef21c646b43f48da9fa41aa100
