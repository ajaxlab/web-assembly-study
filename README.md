# web-assembly-study

https://emscripten.org/docs/getting_started/downloads.html

```
# Get the emsdk repo
git clone https://github.com/emscripten-core/emsdk.git

# Enter that directory
cd emsdk
```

```
# Fetch the latest version of the emsdk (not needed the first time you clone)
git pull

# Download and install the latest SDK tools.
./emsdk install latest

# Make the "latest" SDK "active" for the current user. (writes .emscripten file)
./emsdk activate latest

# Activate PATH and other environment variables in the current terminal
source ./emsdk_env.sh
```

```
Resolving SDK alias 'latest' to '3.1.6'
Resolving SDK version '3.1.6' to 'sdk-releases-upstream-8791c3e936141cbc2dd72d76290ea9b2726d39f3-64bit'
Setting the following tools as active:
   node-14.18.2-64bit
   python-3.9.2-64bit
   releases-upstream-8791c3e936141cbc2dd72d76290ea9b2726d39f3-64bit

Next steps:
- To conveniently access emsdk tools from the command line,
  consider adding the following directories to your PATH:
    /PATH_TO/emsdk
    /PATH_TO/emsdk/node/14.18.2_64bit/bin
    /PATH_TO/emsdk/upstream/emscripten
- This can be done for the current shell by running:
    source "/PATH_TO/emsdk/emsdk_env.sh"
- Configure emsdk in your shell startup scripts by running:
    echo 'source "/PATH_TO/emsdk/emsdk_env.sh"' >> $HOME/.bash_profile

```

```cpp
#include <iostream>

using namespace std;

int main() {
  cout << "[WASM] Loaded" <<endl;
  cout << "Hello Wasm" <<endl;
}

```

```
em++ test.cpp -o test.html
```
