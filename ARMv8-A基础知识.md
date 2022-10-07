# ARMv8-A
本文主要是学习ARMv8-A的基础架构知识，为学习TrustZone技术做铺垫，从而进一步学习TEE(可信执行环境)。TrustZone涉及到了很多异常处理的相关知识，因此需要学习此文档来了解ARM处理器是如何进行异常处理的。学习ARMv8-A的主要参考文档为[ARM Cortex-A Series](https://cs140e.sergio.bz/docs/ARMv8-A-Programmer-Guide.pdf)。希望在完成本笔记后在学习TrustZone时能够理解得更多。

## 指令集
+ ARMv8处理器支持A64 64位指令集，同时也支持32位指令集。与此同时上一代ARMv7处理器只支持32位指令集。
+ 64位指令集能够支持更大的虚拟地址空间。
+ 大物理地址扩展(LPAE)将32位处理器的物理地址扩展到40位，但不扩展虚拟地址空间，即单个应用程序仍然被限制在4GB的内存地址空间内。