# freenom-automatic-renewal（免费域名自动续期）
[![GitHub Stars](https://img.shields.io/github/stars/RouRouX/docker-freenom-automatic-renewal.svg?style=flat-square&label=Stars&logo=github)](https://github.com/RouRouX/docker-freenom-automatic-renewal/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/RouRouX/docker-freenom-automatic-renewal.svg?style=flat-square&label=Forks&logo=github)](https://github.com/RouRouX/docker-freenom-automatic-renewal/fork)
[![Docker Stars](https://img.shields.io/docker/stars/rouroux/freenom-automatic-renewal.svg?style=flat-square&label=Stars&logo=docker)](https://hub.docker.com/r/rouroux/freenom-automatic-renewal)
[![Docker Pulls](https://img.shields.io/docker/pulls/rouroux/freenom-automatic-renewal.svg?style=flat-square&label=Pulls&logo=docker)](https://hub.docker.com/r/rouroux/freenom-automatic-renewal) [![GitHub license](https://img.shields.io/github/license/RouRouX/docker-freenom-automatic-renewal.svg?style=flat-square&label=LICENSE)](https://github.com/RouRouX/docker-freenom-automatic-renewal/blob/master/LICENSE)


## 执行命令：

```
docker run -d --name freenom -v <path to config>:/conf rouroux/freenom-automatic-renewal
```

## 简单说明：

第一次运行容器会在数据卷中建立两个配置文件config.php和.env

修改.env中的freenom的账号信息和邮箱信息，重启容器即可收到邮件，每次启动容器都会执行一次，每天早上9点也会运行一次。

如果想改成只有续期成功才发邮件，修改config.php中'noticeFreq' => 0

详细配置说明查看[项目地址](https://github.com/luolongfei/freenom)

## 最近更新：

2020年6月3日

* 基于 [luolongfei/freenom](https://github.com/luolongfei/freenom/tree/d12e1509d4d6d8e4b158fbcc86bb13fce09d8b3f) 制作镜像

2020年5月30日 

* 基于 [luolongfei/freenom](https://github.com/luolongfei/freenom/tree/0066029871c46394a2cfd4c9b2ba11c521de2da7) 制作镜像

2020年5月9日 
* 基于 [luolongfei/freenom](https://github.com/luolongfei/freenom/tree/1fed4f9c67755f4b75f4d7bf15c550d427984013) 制作镜像
* 增加arm支持

## 没有设备来运行docker镜像？试试利用github actions吧(需要有github账号)
* [actions脚本（注释含简单教程）](https://github.com/RouRouX/freenom/blob/master/.github/workflows/run.yml) 
* [大概原理](https://github.com/luolongfei/freenom/pull/29) 

## 鸣谢：

[luolongfei/freenom](https://github.com/luolongfei/freenom) PHP自动续期脚本项目地址

[oldiy/freenom-automatic-renewal](https://hub.docker.com/r/oldiy/freenom-automatic-renewal) 基于上面脚本的docker镜像地址（此作者很久没更新了，所以才自己写了）

