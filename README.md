# gitbook使用心得
## 常规使用方法
  1.查看node版本  
  node -v
  2.安装命令行工具
  npm install gitbook-cli -g
  3.安装node_modules
  gitbook install
  4.构建，可直接执行5
  gitbook build
  5.启动服务，在localhost:4000查看
  gitbook serve

##坑
  坑1. gitbook语法使用了markdown，图片写法 ！【img】(图片路径)，此处是英文标点，就在这儿图片路径有坑。
      使用最新的gitbook（v3.2.2），本地图片console报错 ，外链图片没事儿，难道还要我找个图床把图片都上传上去吗，真心崩溃~~~~
  坑2. 默认的gitbook生成文件会有facebook等并不需要的模块，可配置book.json文件，
      
      "styles": {
        "website": "styles/website.css"
      }
      
     
  其中，styles中website.css文件内容自行写，参考：
      
      .book .book-body .page-wrapper .page-inner{
          max-width:80% !important;
      }

      .divider,.gitbook-link {
        display: none !important;
      }

      .pull-right{
          display:none!important;
      }

  坑3. 编译后有问题，影响使用。点到【文档说明】的时候，卡住，地址栏url变自己改生成的html。
      尝试方法：试用了各种版本的gitbook（gitbook serve --gitbook=2.0.1），2.0.1/3.1.0，后者甚至都没有报错，但卡住的问题依然存在。
      解决方法：自己改生成完的html去~~~~~ 想哭的冲动没木有，不过解决问题是天理，能看就行。
 

