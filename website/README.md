<!--
    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.
-->

These are the main sources of the website for Apache Beam, hosted at
https://beam.apache.org/.

## About this site

此处为翻译的中文社区官方文档

## Active development

如果您希望预览更改，网站开发需要安装Docker
运行网站测试。

以下命令用于在本地构建和提供网站。

    $ ./gradlew :website:serveWebsite

在本地进行的任何更改都将触发网站的重建。

可以使用以下命令运行网站测试：

    $ ./gradlew :website:testWebsite

## Website push
合并PR后，后台Jenkins作业将自动生成和

推[网站
内容]（https://github.com/apache/beam/tree/asf-site/website/generated-content）
到asf-site分支。 此内容稍后被选中并推送到
https://beam.apache.org/。
## Additional Information

### Writing blog posts
博客文章在`_posts`目录中创建。

如果这是您的第一篇文章，请务必将自己添加到`_data \ authors.yml`。

当您在其标题中列出的发布时间之前处理您的帖子时，
运行Jekyll时添加`--future`以便在本地副本上查看草稿
网站。

### Adding Jekyll plugins

如果您修改站点以使用其他Jekyll插件，请将它们添加到`Gemfile`中
然后运行`bundle update`，它将重新生成完整的`Gemfile.lock`。
确保更新的`Gemfile.lock`包含在pull请求中。 欲获得更多信息，
请参阅Bundler [文档]（http://bundler.io/v1.3/rationale.html）。
