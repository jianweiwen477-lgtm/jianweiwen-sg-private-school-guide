# Jianweiwen 新加坡私校攻略网站

这是一个单页静态网站，用来给学生和家长看新加坡私立学校本科转学、专升本、自己申请、住宿和生活避坑信息。

正式网址计划使用：

https://jianweiwen.vercel.app

## 平时怎么改内容

主要改 `index.html`。改完以后，把 `index.html` 的内容同步复制到 `singapore_private_school_xiaobai.html`，这样本地文件和线上首页会保持一致。

页面里的学校资料主要集中在这些数据块里：

- `schools`：学校名称、地址、专业强项、官方链接。
- `housingMatchData`：每所学校附近住宿区域。
- `nearbyLifeData`：每所学校附近的 MRT、bus stop、公交、美食、food court 和商圈。
- `intakeRows`：入学时间样例。
- `quizBank`：小测验题目和结果。

如果只是改微信、WhatsApp、邮箱，可以直接搜索对应号码或邮箱，然后替换。

## 怎么发布更新

以后建议走 GitHub + Vercel 自动发布：

1. 在 GitHub 仓库里打开 `index.html`。
2. 点编辑，改内容。
3. 写一句简单说明，比如“更新 JCU 附近生活信息”。
4. 提交到主分支。
5. Vercel 会自动重新发布，一般等几十秒到几分钟。
6. 打开 `https://jianweiwen.vercel.app/?v=日期或版本号` 检查，例如 `?v=3`，可以避开微信旧缓存。

## 发布后检查什么

每次更新后至少看这几项：

- 电脑打开首页，不是 404。
- 手机打开首页，导航、卡片、表格没有重叠。
- 微信里打开链接，如果显示旧版，在网址后面加 `?v=新数字`。
- 咨询区的微信、WhatsApp、Email 是否正确。
- 学校官方链接能不能点开。
- 交通路线、营业时间、入学时间这类会变化的信息，最好再用学校官网或地图确认一次。

## 不要上传的东西

GitHub 只需要保存正式文件：

- `index.html`
- `singapore_private_school_xiaobai.html`
- `README.md`
- `.gitignore`

不要上传本地 Vercel 登录文件、token、临时日志、进程文件和缓存文件，比如 `.vercel-cli/`、`com.vercel.cli/`、`*.log`、`*.pid`。
