# lsfg-vk mirror (read-only pointer)

**This repository does not contain the full source code.**

The official repository of **lsfg-vk** (Lossless Scaling Frame Generation on Linux) is hosted by the author at:

- **Primary**: https://git.lsfg-vk.dev/lsfg-vk
- Clone URL: `https://git.lsfg-vk.dev/lsfg-vk.git`

The project is licensed under **CC BY-NC-ND 4.0** (Attribution-NonCommercial-NoDerivatives).  
This means:
- Non-commercial use only
- No derivatives / no modified redistributions
- Attribution required

The author deliberately removed the project from GitHub (and later from Codeberg) because of license restrictions and to avoid AI-generated "slop" forks. Please respect the license and use the official source.

## How to build from source

```bash
# Clone official repository
git clone https://git.lsfg-vk.dev/lsfg-vk.git
cd lsfg-vk

# Optional: checkout a release tag
git checkout tags/2.0.0   # or list tags with: git ls-remote --tags

# Configure (recommended)
cmake -B build -G Ninja \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INTERPROCEDURAL_OPTIMIZATION=ON \
    -DCMAKE_INSTALL_PREFIX=/usr/local \
    -DCMAKE_CXX_COMPILER=clang++ \
    -DLSFGVK_BUILD_UI=ON

# Build
cmake --build build

# Install
sudo cmake --install build
```

### Prerequisites (typical)
- CMake ≥ 3.10
- Ninja
- Clang / GCC with C++20 support
- Vulkan headers & loader
- Qt6 (for UI)
- dxc (DirectX Shader Compiler) if you need to recompile shaders

Official documentation: https://lsfg-vk.dev/docs/installation/building-from-source/

Pre-built binaries: https://builds.lsfg-vk.dev/

Homepage: https://lsfg-vk.dev/

---
*This mirror exists only as a convenience pointer. Always prefer the official git.lsfg-vk.dev repository.*
