# Other Storage

## 项目概述

**Other Storage** 是一个融合存储文件系统，旨在实现对多种云服务和本地存储协议的无缝整合。通过条带化、奇偶校验等技术，该系统能高效地存取数据，并提供统一的访问接口。

## 项目架构

项目的架构由以下几个主要模块组成：

1. **HostProvider**
   - **RestHost**：实现 RESTful API 访问。
   - **SoapHost**：实现 SOAP 服务访问（待实现）。
   - **GrpcHost**: 实现 GRPC 调用访问（待实现）。

2. **SecurityProvider**
   - **OpenSecurity**：实现认证管理与数据的加密和解密功能，确保数据传输和存储的安全性。

3. **StorageProvider**
   - **Raid0Storage**：实现 RAID0 条带化存储策略。
   - **Raid5Storage**：实现 RAID5 容错性存储策略（待实现）。

4. **MemoryProvider**
   - **KvMemory**：实现快速读写，多级存储，自动泄露。

5. **ProtocolProvider**
   - **FTPProtocol**：实现与 FTP 兼容的存储协议。
   - **WebDavProtocol**：实现 WebDAV 协议支持（待实现）。
   - **SFTPProtocol**：实现 SFTP 协议支持（待实现）。
   - **SMBProtocol**：实现 SMB 协议支持（待实现）。
   - **S3Protocol**：实现 AWS S3 协议支持（待实现）。
   - **OneDriveProtocol**：实现 Microsoft OneDrive 协议支持（待实现）。
   - **CloudDriveProtocol**：实现 Google CloudDrive 协议支持（待实现）。
  
6. **LoggerProvider**
   - **Recorder**：实现日志记录功能，支持多种日志级别和输出方式。

7. **ConfigurationProvider**
   - **Configuration**：提供配置管理功能，支持模块化的配置加载。 

## 使用方法

### 安装与运行

1. 确保你的环境中安装了 [.NET SDK](https://dotnet.microsoft.com/download)。
2. 克隆本项目到本地：
   ```bash
   git clone https://github.com/famliars/others.git
   cd storage
   ```
3. 使用命令行构建并运行项目：
   ```bash
   dotnet build
   dotnet run
   ```

### 配置

系统支持通过配置文件进行模块化配置。您可以在项目根目录下创建一个 `config.json` 文件，配置各模块的参数。示例配置如下：

```json
{
  
}
```

### API 文档

通过 REST API 访问系统的各种功能，以下是一些示例 API 调用：

- **获取存储信息**：
  ```
  GET 
  ```

- **上传文件**：
  ```
  POST 
  ```

- **下载文件**：
  ```
  GET 
  ```

## 日志与监控

该系统内置日志功能，可以通过控制台或文件记录系统的运行状态。可以定期调用性能监控模块，查看 CPU 和内存使用情况。


## 贡献

欢迎对本项目进行贡献！请遵循以下步骤：

1. Fork 此仓库。
2. 创建您的特性分支 (`git checkout -b feature/YourFeature`)。
3. 提交更改 (`git commit -m 'Add some feature'`)。
4. 推送到分支 (`git push origin feature/YourFeature`)。
5. 提交 Pull Request。

## 许可证

本项目采用 MIT 许可证，详情请查看 [LICENSE](/LICENSE) 文件。

## 联系

如有疑问或建议，请联系 [Gmail](mailto:light.link.point@gmail.com)。
