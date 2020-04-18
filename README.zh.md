# 我的博客初号机-X0X

#### jekyll 目录结构

> http://jekyllcn.com/docs/structure/

- \_coinfig.yml: 保存配置数据。很多配置选项都可以直接在命令行中进行设置，但是如果你把那些配置写在这儿，你就不用非要去记住那些命令了。

- \_drafts: drafts（草稿）是未发布的文章。这些文件的格式中都没有 title.MARKUP 数据。

- \_includes: 你可以加载这些包含部分到你的布局或者文章中以方便重用。可以用这个标签 {% include file.ext %} 来把文件 \_includes/file.ext 包含进来。用于存放一些固定的 HTML 代码段，文件为.html 格式，可以在模板中通过 liquid 标签引入，常用来在各个模板中复用如 导航条、标签栏、侧边栏 之类的在每个页面上都一样不变的内容，需要注意的是，这个代码段也可以是未被编译的，也就是说也可以使用 liquid 标签放在这些代码段中

- \_layouts 文件夹: layouts（布局）是包裹在文章外部的模板。布局可以在 YAML 头信息中根据不同文章进行选择。 这将在下一个部分进行介绍。标签 {{ content }} 可以将 content 插入页面中。用于存放模板的文件夹，里面有两个模板，default.html 和 post.html

- \_post 文件夹 s: 这里放的就是你的文章了。文件格式很重要，必须要符合: YEAR-MONTH-DAY-title.MARKUP。 永久链接 可以在文章中自己定制，但是数据和标记语言都是根据文件名来确定的.用于存放博客文章的文件夹

- \_data: 格式化好的网站数据应放在这里。jekyll 的引擎会自动加载在该目录下所有的 yaml 文件（后缀是 .yml, .yaml, .json 或者 .csv ）。这些文件可以经由 ｀ site.data ｀ 访问。如果有一个 members.yml 文件在该目录下，你就可以通过 site.data.members 获取该文件的内容。

* \_site: 一旦 Jekyll 完成转换，就会将生成的页面放在这里（默认）。最好将这个目录放进你的 .gitignore 文件中。

* .jekyll-metadata: 该文件帮助 Jekyll 跟踪哪些文件从上次建立站点开始到现在没有被修改，哪些文件需要在下一次站点建立时重新生成。该文件不会被包含在生成的站点中。将它加入到你的 .gitignore 文件可能是一个好注意。

* 其他一些未被提及的目录和文件如 css 还有 images 文件夹， favicon.ico 等文件都将被完全拷贝到生成的 site 中。这里有一些使用 Jekyll 的站点，如果你感兴趣就来看看吧。

* css 文件夹: 存放博客所用 css 的文件夹

* image 和 js 等自定义文件夹：用来存放一些需要的资源文件，如图片或者 javascript 文件，可以任意命名

* CNAME 文件：用来在 github 上做域名绑定的

#### _config.yml配置
> http://jekyllcn.com/docs/configuration/