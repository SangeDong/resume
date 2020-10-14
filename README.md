## 一份优雅简约的简历
- 优化构建，页面秒开无闪烁
- 自适应屏幕兼容移动端
- Github Action自动部署部署到ghpages，可在线浏览
- 自动生成 PDF，全自动化流程

## 使用
1. fork本项目后再clone到本地修改
2. 进入项目目录执行`npm i`安装依赖
3. 执行`npm run dev`开始开发，根据你的情况修改`src/index.html`里的内容

## 部署
项目使用`GitHub Actions`构建部署,修改如下
1. 替换`webpack-dist.config.js`文件里的`resume.sangedon.cn`为你自己的域名，并根据[该文档配置你的域名解析](https://help.github.com/cn/github/working-with-github-pages/about-custom-domains-and-github-pages)
2. 参照[官方文档](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/creating-a-personal-access-token)生成一个密钥。然后，将这个密钥储存到当前仓库的Settings/Secrets里面。
4. 将上一步创建的ACCESS_TOKEN替换掉`workflows/pub.yml`中`github_token`中secrets变量后的内容，替换后为`github_token:secrets.ACCESS_TOKEN`
3. 修改完后push到master分支，Github Action会自动部署
