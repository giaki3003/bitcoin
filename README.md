# Forknet Guide
Setup and testing instructions for Forknet

## Dependencies: (Setting this all up in a linux VM is suggested)
- electrum server 
- flutter sdk
- rustup, rust, cargo
- buf_curl or grpcurl
- enforcer + forknet support
- bitwindow + forknet support
- drivechain-forknet (bitcoin 31.x + drivechain fork)

## drivechain-forknet build instructions (example uses ubuntu LTS (24.04)) 
Install build dependencies: 
```git cmake build-essential lisqlite3-dev libboost-all-dev libzmq3-dev pkgconf```

Build:
```
cmake -B build -DBUILD_GUI=OFF -DBUILD_BENCH=OFF -DBUILD_FUZZ_BINARY=OFF -DBUILD_GUI_TESTS=OFF -DBUILD_TESTS=OFF -DENABLE_IPC=OFF -DWITH_ZMQ=ON -DBUILD_UTIL=ON
cmake --build build -j $(nproc)
```


## Data directories & config files:
```
// Windows: C:\Users\Username\AppData\Local\drivechain-forknet
// macOS: ~/Library/Application Support/drivechain-forknet
// Unix-like: ~/.drivechain-forknet
```
Config file name: ```drivechain-forknet.conf```


# Forknet changes:
- [ ] OP_DRIVECHAIN
- [ ] OP_RETURN unlimited
- [ ] Difficulty reset at block #0
- [ ] Optional transaction replay protection
- [ ] Block size decreased
- [ ] SHAD
