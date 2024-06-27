### C4668 
**UE版本**  4.27.2 </br>
**VS版本**  2022 </br>
**发现日期**: 2024.6.27</br>
**报错信息**：</br>
</br>
1>C:\Program Files (x86)\Windows Kits\10\include\10.0.22621.0\winrt\wrl/event.h(211): error C4668: 没有将“_NOEXCEPT_TYPES_SUPPORTED”定义为预处理器宏，用“0”替换“#if/#elif” </br>
1>C:\Program Files (x86)\Windows Kits\10\include\10.0.22621.0\winrt\wrl/event.h(211): error C4668: 没有将“__cpp_noexcept_function_type”定义为预处理器宏，用“0”替换“#if/#elif” </br>
1>C:\Program Files (x86)\Windows Kits\10\include\10.0.22621.0\winrt\wrl/event.h(371): error C4668: 没有将“_NOEXCEPT_TYPES_SUPPORTED”定义为预处理器宏，用“0”替换“#if/#elif” </br>
1>C:\Program Files (x86)\Windows Kits\10\include\10.0.22621.0\winrt\wrl/event.h(371): error C4668: 没有将“__cpp_noexcept_function_type”定义为预处理器宏，用“0”替换“#if/#elif” </br>

**解决方案**：</br>

找到HoloLensTargetPlatform.Build.cs
加上
```
bEnableUndefinedIdentifierWarnings = false;
```
![](https://github.com/Eric-Monkey/memo/blob/main/Imgs/Example.png) </br>


### C4834
**UE版本** 4,27.2</br>
**VS版本** 2022</br>
**报错信息**:</br>
**发现日期**: 2024.6.27</br>
1>D:/UE/UnrealEngine-4.27.2-release/Engine/Plugins/Runtime/Steam/SteamVR/Source/SteamVRInputDevice/Private/SteamVRInputDeviceFunctionLibrary.cpp(511): error C4834: 放弃具有 [[nodiscard]] 属性的函数的返回值</br>
**解决方案**:<br>
```
//找到文件SteamVRInputDeviceFunctionLibrary.cpp  添加代码
#pragma warning(disable : 4834)
```
![](https://github.com/Eric-Monkey/memo/blob/main/Imgs/Example1.png) </br>
