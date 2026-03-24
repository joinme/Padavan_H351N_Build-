# H351N 百米路由器3 Padavan 单频固件

## 硬件规格
- SoC: MediaTek MT7620A @ 580MHz
- RAM: 128MB DDR2
- Flash: 16MB SPI NOR
- 无线: 2.4G 300Mbps（内置 2T2R，无 5G）
- 网口: 1× WAN + 4× LAN（百兆）
- USB: 1× USB 2.0

## 下载固件
进入 [Actions](../../actions) 页面，选择最新成功的编译，下载 `H351N-Padavan-Firmware` 产物。

## 刷机步骤
1. 进入 Breed 恢复模式（按住 Reset 键上电，灯闪后松开）
2. 浏览器访问 http://192.168.1.1
3. 选择"固件更新" → 选择下载的 `.trx` 文件
4. 点击上传，等待刷入完成（约 2-3 分钟）
5. 自动重启后，访问 http://192.168.123.1 管理页面

## 默认账号
- 用户名: `admin`
- 密码: `admin`

## 注意事项
- 本固件移除 MT7612E 5G 驱动，仅保留 2.4G 无线
- 刷机前请通过 Breed 备份原厂 EEPROM
- 如遇无线异常，可尝试恢复原厂 EEPROM 后重刷

## 自行编译
Fork 本仓库，修改 `.github/workflows/build-h351n.yml`，推送后自动编译。# Padavan_H351N_Build-
