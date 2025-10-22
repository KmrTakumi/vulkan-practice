# Drawing a triangle
Vulkan Tutorial: https://docs.vulkan.org/tutorial/latest/03_Drawing_a_triangle/00_Setup/00_Base_code.html

## Compiling from the terminal on macOS
Add vulkan SDK to ~/.zshrc
```zsh
export VULKAN_SDK=$HOME/VulkanSDK/1.4.321.0/macOS
export DYLD_LIBRARY_PATH=$VULKAN_SDK/lib:$DYLD_LIBRARY_PATH
export PATH=$VULKAN_SDK/bin:$PATH
export VK_ICD_FILENAMES=$VULKAN_SDK/share/vulkan/icd.d/MoltenVK_icd.json
export VK_LAYER_PATH=$VULKAN_SDK/share/vulkan/explicit_layer.d
```
Apply the changes:
```zsh
source ~/.zshrc
```
Compile (g++/clang++)
```zsh
g++ 01-triangle.cpp -std=c++20 -I/opt/homebrew/include -I"$VULKAN_SDK/include" -L/opt/homebrew/lib -L"$VULKAN_SDK/lib" -lglfw -lvulkan 
```
If DYLD_LIBRARY_PATH is not set, add:
```zsh
-Wl,-rpath,"$VULKAN_SDK/lib"
```