# 云原生个人博客自动化部署项目

## 项目简介

本项目演示了如何在阿里云ECS上，使用Docker容器化技术全自动部署一个高可用的WordPress个人博客。涵盖了从云服务器配置、Docker环境搭建到应用部署的完整DevOps流程。

## 技术栈

- **云平台**: 阿里云 ECS
- **容器化**: Docker, Docker Compose
- **Web应用**: WordPress
- **数据库**: MySQL 5.7
- **自动化**: Shell脚本, Docker Compose编排

## 项目功能

- ✅ 云服务器(ECS)初始化与配置
- ✅ Docker & Docker Compose 环境安装
- ✅ 使用Docker Compose编排多容器应用(WordPress + MySQL)
- ✅ 配置数据卷实现数据持久化
- ✅ 配置阿里云安全组规则，开放网络访问
- ✅ 一键式部署与启动

## 架构图
用户浏览器
↓ (HTTP请求)
阿里云ECS实例:80端口
↓ (端口映射)
Docker容器: WordPress (Apache/PHP)
↓ (容器网络)
Docker容器: MySQL 5.7

text

## 快速开始

### 环境要求
- 阿里云ECS实例（Ubuntu 20.04 LTS）
- 已配置安全组入方向规则，允许HTTP(80)端口访问

### 部署步骤

1. **克隆项目到服务器**
```bash
git clone https://github.com/Soelcc/my-cloud-blog.git
cd my-cloud-blog
一键部署启动所有服务

bash
docker compose up -d
访问应用
在浏览器中访问您的ECS实例公网IP地址（例如：http://your-server-ip）来完成WordPress的安装。

部署过程与关键技术点
1. Docker环境配置
在Ubuntu系统上安装Docker Engine和Docker Compose。

解决了国内网络环境拉取Docker官方镜像缓慢的问题。

2. 应用编排与配置
使用docker-compose.yml文件定义并管理WordPress和MySQL服务。

配置环境变量实现容器间的通信（如数据库连接信息）。

使用Docker数据卷(volumes)确保数据库和WordPress文件持久化存储。

3. 云平台网络配置
在阿里云控制台配置安全组(Security Group)，确保80端口对公网开放。

这是服务能够从外部访问的关键步骤。

项目总结与收获
通过完成本项目，我系统性地实践并掌握了以下核心技能：
Linux云服务器运维：包括ECS的基本操作、系统配置和权限管理。
容器化技术：Docker和Docker Compose的实际应用，理解镜像、容器、网络和数据卷的概念。
服务编排：使用Compose定义和管理多容器应用架构。
云平台网络知识：理解并配置虚拟网络(VPC)、安全组等关键网络概念。
问题排查能力：在部署过程中独立解决了包括网络连通性、配置错误在内的多种技术问题。


如果这个项目对您有帮助，欢迎在Git仓库点个Star！
