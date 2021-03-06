# mp3tag-douban-id3-plugins v2.5
十年前写过一个 [Mp3tag](https://www.mp3tag.de/en/download.html) 的[插件](https://www.appinn.com/mp3tag-douban-id3-plugins/)，最近装修打算放个数播，发觉十年过去了，PC上依然没有很好的方法更新id3，趁着豆瓣 API V2 还勉强能用，赶紧用，基于新的 Mp3tag [Web Sources Framework](https://help.mp3tag.de/main_online.html) 更新一个 JSON 插件版本。做了十年PM，这次好好写写文档很重要。



#### Release Note

2020-10-06（v2.5）:

- 支持豆瓣音乐 API V2
- 支持豆瓣音乐模糊查询
- 查询结果页支持豆瓣评分、专辑名、艺术家、发行年份、版本、介质和厂牌
- 支持豆瓣音乐CDN封面Large大图
- 调整标签附加了豆瓣评分、豆瓣链接，豆瓣ID
- 注释保留了豆瓣音乐的Tags拼接
- 支持有序，无序标点的音轨顺序和去空格名称



#### 暂无支持项

- 搜索结果不支持显示音轨数量
- 调整标签不支持流派
- 未支持专辑集艺术家、作曲家和CD号



#### 安装方法

找到 `%appdata%\mp3tag\data\sources` 位置，下载 [release](https://github.com/yoyicue/mp3tag-douban-id3-plugins/releases) 版本或者把最新的 [DoubanMusic.src](https://raw.githubusercontent.com/yoyicue/mp3tag-douban-id3-plugins/main/DoubanMusic.src) 直接粘贴在这个目录下，重启 Mp3tag 即可



#### 使用方式

1. 安装成功后，工具栏`标签数据源(S)` 下会有 `DoubanMusic` 选项

2. 点击 `下一步(N)>` 后会弹出一个查询条件的搜索框，写着`专辑集`，但这里是模糊查询，可以 `“歌手 专辑名”` 

3. 在豆瓣音乐搜索成功后会让你选择一个结果，豆瓣返回结果的上限是100条，所以精准搜索很关键

4. 相同的CD有不同的介质版本，比如CD，黑胶等等，还有不同的厂牌，热门CD可能还会有较多结果

5. 可以按表头 `Rating`（豆瓣评分）作为一个参考，不放心可以点击 `预览`跳转到豆瓣页面看看

6. 选好了点击 `下一步(N)>` 会进入调整标签信息页面，检查完毕 `确认(O)` 即可

   

#### 调整时注意事项

1. `流派`、`注释`和`音轨`三个点格外注意
2. Comments （注释）我把豆瓣音乐的 Tags 用逗号做了拼接，方便对音乐做参考，不喜可手动清空
3. 豆瓣音乐没有结构化的 Genre （流派）信息，需要自己判断填入，注释的流派标签对这里是个参考
4. 豆瓣音乐的Track（音轨）也没有结构化，大小写，有序标签，无序标签都有，当前版本都做了一定的支持
5. 但音轨没有如果遇到没有支持很好的文本格式，可以提交Issue。



感谢小众软件和青蛙 @scavin，基于对自己的判断，虽然是一个很小的脚本，但是依然不能保证有资源迭代。见谅。

#### 历史版本和链接
- https://code.google.com/archive/p/cunfe/
- https://www.appinn.com/mp3tag-douban-id3-plugins/
- https://www.douban.com/group/topic/5183124/ （ID已注销）
