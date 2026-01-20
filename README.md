# Lighthouse - IDA 9.0 Compatible Version

> **⚠️ 注意**: 这是 Lighthouse 的 IDA Pro 9.0 兼容性修复版本
> 
> **原项目**: [gaasedelen/lighthouse](https://github.com/gaasedelen/lighthouse)
> 
> **原作者**: Markus Gaasedelen ([@gaasedelen](https://twitter.com/gaasedelen))

---

## 关于本版本

本版本修复了 Lighthouse 插件在 IDA Pro 9.0 中的兼容性问题。IDA Pro 9.0 对其 Python API 进行了重大重构，移除了许多旧别名，导致原版插件无法在 IDA 9.0 中正常运行。

### 主要修复

- ✅ **修复 `eclose` 函数导入问题** - 适配 IDA 9.0 中 `eclose` 从 `idaapi` 移动到 `ida_diskio` 的变化
- ✅ **修复 Python 语法警告** - 修复了无效转义序列的警告
- ✅ **保持向后兼容** - 完全兼容 IDA 7.x、8.x 和 9.0+

### 详细修改说明

完整的修改说明请查看：
- [IDA9_COMPATIBILITY_CN.md](IDA9_COMPATIBILITY_CN.md) - 中文详细说明

## 安装

### IDA Pro 安装

1. 从 IDA 的 Python 控制台运行以下命令查找插件目录：
   ```python
   import idaapi, os; print(os.path.join(idaapi.get_user_idadir(), "plugins"))
   ```

2. 将此仓库的 `/plugins/` 文件夹内容复制到上述目录

3. 重启 IDA Pro

### 支持的版本

- ✅ IDA Pro 7.x
- ✅ IDA Pro 8.x  
- ✅ **IDA Pro 9.0+** (本版本主要修复)

## 使用

安装完成后，在 IDA Pro 的菜单中会出现新的 Lighthouse 入口。详细使用方法请参考[原项目文档](https://github.com/gaasedelen/lighthouse)。

## 许可证

本项目遵循原项目的 MIT 许可证。详见 [LICENSE](LICENSE) 文件。

---

**原项目链接**: https://github.com/gaasedelen/lighthouse
