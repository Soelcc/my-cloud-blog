# 云原生个人博客自动化部署项目

## 项目简介

本项目演示了如何在阿里云ECS上，使用Docker容器化技术全自动部署一个高可用的WordPress个人博客。涵盖了从云服务器配置到应用部署的完整DevOps流程。

## 技术栈

- 云平台: 阿里云 ECS
- 容器化: Docker, Docker Compose
- Web应用: WordPress
- 数据库: MySQL 5.7
- 自动化: Shell Script, Docker Compose

## 项目功能

- 云服务器环境配置
- Docker & Docker Compose 安装
- 多容器应用编排（WordPress + MySQL）
- 数据持久化配置
- 网络与安全组配置
- 一键部署脚本

## 架构图

用户访问 → 阿里云ECS(80端口) → Docker容器(WordPress) → Docker容器(MySQL)

## 快速开始

### 环境要求
- 阿里云ECS实例（Ubuntu 20.04+）
- 安全组开放80端口

### 部署步骤

1. 克隆项目：
git clone https://gitee.com/Sonic1178/my-cloud-blog.git
cd my-cloud-blog

2. 一键部署：
docker compose up -d

3. 访问应用：
打开浏览器访问 http://118.178.99.8

## 部署过程记录

### 遇到的问题及解决方案

1. Docker镜像拉取超时
问题: 国内网络无法访问Docker Hub
解决方案: 
- 配置国内镜像加速器
- 使用华为云镜像站直接拉取

2. 安全组配置
问题: 服务运行但无法外网访问
解决方案: 在阿里云安全组中添加80端口入站规则

3. YAML语法错误
问题: docker-compose.yml格式错误
解决方案: 重新创建文件，确保缩进和语法正确

## 学习收获

通过本项目，掌握了：
- 云服务器运维管理
- Docker容器化技术
- 多服务应用编排
- 云平台网络配置
- 问题排查与解决能力

如果这个项目对你有帮助，请给个星标支持！
