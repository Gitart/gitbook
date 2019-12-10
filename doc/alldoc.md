# Как использовать систему управления версиями Git в Linux. Всеобъемлющее руководство.

27.11.2019[Егор Мирошниченко](http://blog.sedicomm.com/author/y-myroshnichenko/) [GIT](http://blog.sedicomm.com/category/linux/git/)[Комментариев нет](http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/#respond)

[](#)

*   [Facebook](https://www.facebook.com/sharer/sharer.php?u=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&t=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [Twitter](#)
*   [Google+](https://plus.google.com/share?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Pinterest](#)
*   [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&ro=true&trk=EasySocialShareButtons&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Digg](http://digg.com/submit?phase=2amp;url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [Del](https://del.icio.us/login?log=out&provider=essb&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&v=5)
*   [StumbleUpon](http://www.stumbleupon.com/badge/?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Tumblr](https://www.tumblr.com/widgets/share/tool?canonicalUrl=http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&posttype=link)
*   [VKontakte](https://vkontakte.ru/share.php?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&description=&image=)
*   [Print](#)
*   [Email](#)
*   [Flattr](https://flattr.com/submit/auto?user_id=&url=http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F&title=%25D0%259A%25D0%25B0%25D0%25BA%2B%25D0%25B8%25D1%2581%25D0%25BF%25D0%25BE%25D0%25BB%25D1%258C%25D0%25B7%25D0%25BE%25D0%25B2%25D0%25B0%25D1%2582%25D1%258C%2B%25D1%2581%25D0%25B8%25D1%2581%25D1%2582%25D0%25B5%25D0%25BC%25D1%2583%2B%25D1%2583%25D0%25BF%25D1%2580%25D0%25B0%25D0%25B2%25D0%25BB%25D0%25B5%25D0%25BD%25D0%25B8%25D1%258F%2B%25D0%25B2%25D0%25B5%25D1%2580%25D1%2581%25D0%25B8%25D1%258F%25D0%25BC%25D0%25B8%2BGit%2B%25D0%25B2%2BLinux.%2B%25D0%2592%25D1%2581%25D0%25B5%25D0%25BE%25D0%25B1%25D1%258A%25D0%25B5%25D0%25BC%25D0%25BB%25D1%258E%25D1%2589%25D0%25B5%25D0%25B5%2B%25D1%2580%25D1%2583%25D0%25BA%25D0%25BE%25D0%25B2%25D0%25BE%25D0%25B4%25D1%2581%25D1%2582%25D0%25B2%25D0%25BE.&description=%D0%A3%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+%28%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D1%8C+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B9%29+--+%D1%8D%D1%82%D0%BE+%D1%81%D0%BF%D0%BE%D1%81%D0%BE%D0%B1+%D0%B7%D0%B0%D0%BF%D0%B8%D1%81%D0%B8+%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B9+%D0%B2+%D1%84%D0%B0%D0%B9%D0%BB+%D0%B8%D0%BB%D0%B8+%D1%81%D0%B1%D0%BE%D1%80+%D1%84%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2+%D1%81+%D1%82%D0%B5%D1%87%D0%B5%D0%BD%D0%B8%D0%B5%D0%BC+%D0%B2%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%B8%2C+%D1%87%D1%82%D0%BE%D0%B1%D1%8B+%D0%BF%D0%BE%D0%B7%D0%B6%D0%B5+%D0%B2%D1%8B+%D0%BC%D0%BE%D0%B3%D0%BB%D0%B8+%D0%BF%D1%80%D0%BE%D1%81%D0%BC%D0%BE%D1%82%D1%80%D0%B5%D1%82%D1%8C+%D0%BA%D0%BE%D0%BD%D0%BA%D1%80%D0%B5%D1%82%D0%BD%D1%8B%D0%B5+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B8.+%D0%A1%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+%28VCS%29+--+%D1%8D%D1%82%D0%BE+%D0%B8%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BC%D0%B5%D0%BD%D1%82%2C+%D0%BA%D0%BE%D1%82%D0%BE%D1%80%D1%8B%D0%B9+%D0%B7%D0%B0%D0%BF%D0%B8%D1%81%D1%8B%D0%B2%D0%B0%D0%B5%D1%82+%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2+%D1%84%D0%B0%D0%B9%D0%BB%D1%8B+%D0%B2+%D1%84%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2%D0%BE%D0%B9+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B5.+%D0%A1%D1%83%D1%89%D0%B5%D1%81%D1%82%D0%B2%D1%83%D0%B5%D1%82+%D0%BC%D0%BD%D0%BE%D0%B6%D0%B5%D1%81%D1%82%D0%B2%D0%BE+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC+%D0%BA%D0%BE%D0%BD%D1%82%D1%80%D0%BE%D0%BB%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D0%B9%2C+%D0%BD%D0%BE+Git+%D0%B2+%D0%BD%D0%B0%D1%81%D1%82%D0%BE%D1%8F%D1%89%D0%B5%D0%B5+%D0%B2%D1%80%D0%B5%D0%BC%D1%8F+%D1%8F%D0%B2%D0%BB%D1%8F%D0%B5%D1%82%D1%81%D1%8F+%D1%81%D0%B0%D0%BC%D1%8B%D0%BC+%D0%BF%D0%BE%D0%BF%D1%83%D0%BB%D1%8F%D1%80%D0%BD%D1%8B%D0%BC+%D0%B8+%D1%87%D0%B0%D1%81%D1%82%D0%BE+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D1%83%D0%B5%D0%BC%D1%8B%D0%BC+%D1%80%D0%B5%D1%88%D0%B5%D0%BD%D0%B8%D0%B5%D0%BC%2C+%D0%BE%D1%81%D0%BE%D0%B1%D0%B5%D0%BD%D0%BD%D0%BE+%D0%B4%D0%BB%D1%8F+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+%D0%B8%D1%81%D1%85%D0%BE%D0%B4%D0%BD%D0%BE%D0%B3%D0%BE+%D0%BA%D0%BE%D0%B4%D0%B0.+%D0%A3%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+%D0%BC%D0%BE%D0%B6%D0%B5%D1%82+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C%D1%81%D1%8F+%D0%BF%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8+%D0%B4%D0%BB%D1%8F+%D0%BB%D1%8E%D0%B1%D0%BE%D0%B3%D0%BE+%D1%82%D0%B8%D0%BF%D0%B0+%D1%84%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2+%D0%BD%D0%B0+%D0%BA%D0%BE%D0%BC%D0%BF%D1%8C%D1%8E%D1%82%D0%B5%D1%80%D0%B5%2C+%D0%B0+%D0%BD%D0%B5+%D1%82%D0%BE%D0%BB%D1%8C%D0%BA%D0%BE+%D0%B4%D0%BB%D1%8F+%D0%B8%D1%81%D1%85&language=sq_AL&tags=Branch%2Ccommit%2CCVCS%2CDiff%2CDVCS%2CGit%2CGithub%2Clinux%2Clog%2Cmerge%2Cpull%2Cpush%2Cshow%2Cssh%2CVCS&hidden=0&category=text)
*   [Reddit](http://reddit.com/submit?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [Buffer](https://bufferapp.com/add?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&text=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&via=&picture=&count=horizontal&source=button)
*   [Love This](#)
*   [Weibo](http://service.weibo.com/share/share.php?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&pic=http://blog.sedicomm.com/wp-content/uploads/2018/10/How-to-Use-Git-Version-Control-System-in-Linux.png)
*   [Pocket](https://getpocket.com/save?title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&url=http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F)
*   [Xing](https://www.xing.com/social_plugins/share?h=1;url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Odnoklassniki](https://connect.ok.ru/offer?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&imageUrl=http://blog.sedicomm.com/wp-content/uploads/2018/10/How-to-Use-Git-Version-Control-System-in-Linux.png)
*   [ManageWP.org](http://managewp.org/share/form?url=http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F)
*   [WhatsApp](whatsapp://send?text=Как%20использовать%20систему%20управления%20версиями%20Git%20в%20Linux.%20Всеобъемлющее%20руководство.%20http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F)
*   [Meneame](http://www.meneame.net/submit.php?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Blogger](https://www.blogger.com/blog_this.pyra?t&u=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&n=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [Amazon](http://www.amazon.com/gp/wishlist/static-add?u=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&t=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [Yahoo Mail](http://compose.mail.yahoo.com/?body=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Gmail](https://mail.google.com/mail/u/0/?view=cm&fs=1&su=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&body=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&ui=2&tf=1)
*   [AOL](http://webmail.aol.com/Mail/ComposeMessage.aspx?subject=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&body=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Newsvine](http://www.newsvine.com/_tools/seed&save?u=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&h=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [HackerNews](https://news.ycombinator.com/submitlink?u=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&t=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [Evernote](http://www.evernote.com/clip.action?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [MySpace](https://myspace.com/post?u=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Mail.ru](http://connect.mail.ru/share?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&description=)
*   [Viadeo](https://www.viadeo.com/?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [Line](https://social-plugins.line.me/lineit/share?url=http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F)
*   [Flipboard](https://share.flipboard.com/bookmarklet/popout?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.)
*   [Comments](#comments)
*   [Yummly](http://www.yummly.com/urb/verify?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&image=http://blog.sedicomm.com/wp-content/uploads/2018/10/How-to-Use-Git-Version-Control-System-in-Linux.png&yumtype=button)
*   [SMS](sms:&body=Как%20использовать%20систему%20управления%20версиями%20Git%20в%20Linux.%20Всеобъемлющее%20руководство.%20http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F)
*   [Viber](viber://forward?text=Как%20использовать%20систему%20управления%20версиями%20Git%20в%20Linux.%20Всеобъемлющее%20руководство.%20http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F)
*   [Telegram](tg://msg?text=Как%20использовать%20систему%20управления%20версиями%20Git%20в%20Linux.%20Всеобъемлющее%20руководство.%20http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F)
*   [Subscribe](#)
*   [Skype](https://web.skype.com/share?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Facebook Messenger](fb-messenger://share/?link=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Kakao](https://story.kakao.com/share?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [LiveJournal](http://www.livejournal.com/update.bml?subject=Как использовать систему управления версиями Git в Linux. Всеобъемлющее руководство.&event=%3Ca+href%3D%22http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F%22%3E%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.%3C%2Fa%3E)
*   [Yammer](https://www.yammer.com/messages/new?login=true&trk_event=yammer_share&status=Как%20использовать%20систему%20управления%20версиями%20Git%20в%20Linux.%20Всеобъемлющее%20руководство. http%3A%2F%2Fblog.sedicomm.com%2F2019%2F11%2F27%2Fkak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo%2F)
*   [Edgar](javascript:(function()%7B!function()%7Bvar e%3Ddocument.getElementsByTagName("head")%5B0%5D,t%3Ddocument.createElement("script")%3Bt.type%3D"text/javascript",t.src%3D"//app.meetedgar.com/share.js%3F"%2BMath.floor(99999*Math.random()),e.appendChild(t)%7D()%7D)()%3B)
*   [Fintel](https://fintel.io/submit?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Mix](https://mix.com/add?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/)
*   [Instapaper](https://www.instapaper.com/hello2?url=http://blog.sedicomm.com/2019/11/27/kak-ispolzovat-sistemu-upravleniya-versiyami-git-v-linux-vseobemlyushhee-rukovodstvo/&title=%D0%9A%D0%B0%D0%BA+%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D1%8C+%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%83+%D1%83%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F+%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F%D0%BC%D0%B8+Git+%D0%B2+Linux.+%D0%92%D1%81%D0%B5%D0%BE%D0%B1%D1%8A%D0%B5%D0%BC%D0%BB%D1%8E%D1%89%D0%B5%D0%B5+%D1%80%D1%83%D0%BA%D0%BE%D0%B2%D0%BE%D0%B4%D1%81%D1%82%D0%B2%D0%BE.&description=)

x

[![](http://blog.sedicomm.com/wp-content/uploads/2019/08/blog-linux-book-a-z.png)](http://edu-cisco.org/linux-commands-form-a-to-z-handbook-with-examples/?utm_source=blog.sedicomm.com&utm_medium=LinuxAZ&utm_campaign=blog)

Управление версиями (контроль версий) — это способ записи изменений в файл или сбор файлов с течением времени, чтобы позже вы могли просмотреть конкретные версии. Система управления версиями (**VCS**) — это инструмент, который записывает изменения в файлы в файловой системе.

Существует множество систем контроля версий, но **Git** в настоящее время является самым популярным и часто используемым решением, особенно для управления версиями исходного кода. Управление версиями может использоваться практически для любого типа файлов на компьютере, а не только для исходного кода.

Системы управления версиями предлагают несколько функций, которые позволяют отдельным лицам или группе людей:

*   создавать версии проекта.
*   отслеживать изменения и разрешать конфликты.
*   выполнять слияние изменений в общую версию.
*   выполнять откат и отмену изменений выбранных файлов или всего проекта.
*   иметь доступ к основным версиям проекта для сравнения изменений с течением времени.
*   просматривать, кто последний проводил изменения файла, что могло вызвать проблему.
*   создавать безопасную резервную копию проекта.
*   использовать несколько машин для работы над одним проектом и многое другое.

Проект под управлением системы контроля версий, такой как **Git**, будет состоять в основном из трех разделов, а именно:

*   **репозиторий**: база данных для записи состояния или изменения файлов проекта. Он содержит все необходимые метаданные **Git** и объекты для нового проекта. Обратите внимание, что это обычно то, что копируется при клонировании репозитория с другого компьютера на сетевом или удаленном сервере.
*   **рабочий** **каталог** или **область**: хранит копию файлов проекта, с которыми вы можете работать (дополнять, удалять и выполнять другие действия по модификации).
*   **промежуточная область:** файл (известный как **index under Git**) в каталоге **Git**, который хранит информацию об изменениях, которые вы готовы закомитить (сохранить состояние файла или набора файлов) в репозиторий.

Существует два основных типа **VCS**, причем основным их отличием является количество репозиториев:

*   **Централизованные** **системы** **управления** **версиями** (**CVCS**): здесь каждый член команды проекта получает свой собственный локальный рабочий каталог, однако они вносят изменения только в один центральный репозиторий.
*   **Системы управления распределенной версией** (**DVCS**): здесь каждый член команды проекта получает свой собственный локальный рабочий каталог и каталог **Git**, где он может совершать коммиты. После того, как человек коммитит что\-то локально, другие члены команды не могут получить доступ к изменениям, пока он/она не выкладывает их в центральный репозиторий. **Git** является примером **DVCS**.

Кроме того, репозиторий **Git** может быть «**bare**» (репозиторий, который не имеет рабочего каталога) или «**non\-bare**» (с одним рабочим каталогом). **Shared** (или публичные) хранилища всегда должны быть **bare** — все репозитории **Github** являются **bare**.

 [![](http://blog.sedicomm.com/wp-content/uploads/2019/08/blog-ipv6.png)](http://edu-cisco.org/it-admin-video-lessons/?utm_source=blog.sedicomm.com&utm_medium=IPv6&utm_campaign=blog)

#### Изучим контроль версий с Git

**Git** — бесплатная, открытая, быстрая, мощная, распределенная, простая в использовании и популярная система управления версиями, которая очень эффективна при работе с большими проектами и имеет замечательную систему ветвления и слияния. Она предназначен для обработки данных, как серия мини\-файловой системы, которая хранится в каталоге **Git**.

Рабочий процесс с использованием **Git** очень прост: вы вносите изменения в файлы в своем рабочем каталоге, а затем выборочно добавляете только те файлы, которые были изменены, в промежуточную область, которая станет частью вашего следующего коммита.

После того, как вы готовы, вы совершите коммит, который берет файлы из промежуточной области и сохраняет их навсегда в каталоге **Git**.

Чтобы установить **Git** в **Linux**, используйте соответствующую команду для вашего дистрибутива:

```
$ sudo apt install git [On Debian/Ubuntu]
$ sudo yum install git [On CentOS/RHEL]
```

После установки **Git** рекомендуется сообщить **Git**, информацию о вас, предоставив свое полное имя и адрес электронной почты, следующим образом:

```
$ git config --global user.name “Alex Udaff”
$ git config --global user.email “alex.udaff@gmail.com”
```

Чтобы проверить настройки **Git**, используйте следующую команду:

```
$ git config --list
```

 [![](http://blog.sedicomm.com/wp-content/uploads/2019/07/blog-free-education.png)](http://edu-cisco.org/it-admin-video-lessons/?utm_source=blog.sedicomm.com&utm_medium=ItAdminVideoLessons&utm_campaign=blog)

[![View-Git-Settings](http://blog.sedicomm.com/wp-content/uploads/2018/10/View-Git-Settings.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/View-Git-Settings.png)

#### Создадим новый репозиторий Git

Общие репозитории или централизованные рабочие репозитории очень распространены, мы здесь это продемонстрируем. Например, мы предполагаем, что вам было поручено настроить удаленный общий репозиторий для системных администраторов/программистов из разных отделов вашей организации, для работы над проектом под названием **bashscripts**, который будет храниться в **/projects/scritpts/** на сервере.

Создайте **SSH** на удаленном сервере и необходимый каталог, затем создайте группу под названием **sysadmins** (добавьте всех членов команды проекта в эту группу, например, **user** **admin**), и установите соответствующие разрешения для этого каталога.

```
# mkdir-p /projects/scripts/
# groupadd sysadmins
# usermod -aG sysadmins admin
# chown :sysadmins -R /projects/scripts/
# chmod 770 -R /projects/scripts/
```

Затем инициализируйте **bare** (пустой) репозиторий проекта:

```
# git init --bare /projects/scripts/bashscripts
```

[![Initialize-Git-Shared-Repository](http://blog.sedicomm.com/wp-content/uploads/2018/10/Initialize-Git-Shared-Repository.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Initialize-Git-Shared-Repository.png)

На этом этапе вы успешно инициализировали пустой каталог **Git,** который является центральным хранилищем для проекта. Попробуйте создать список каталогов, чтобы увидеть все файлы и каталоги:

```
# ls -la /projects/scripts/bashscripts/
```

[![List-Git-Shared-Repository](http://blog.sedicomm.com/wp-content/uploads/2018/10/List-Git-Shared-Repository.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/List-Git-Shared-Repository.png)

#### Клонирование хранилища Git

Теперь клонируйте удаленный общий репозиторий **Git** на локальный компьютер через **SSH** (вы также можете выполнить клонирование через **HTTP**/**HTTPS**, если у вас установлен и настроен веб\-сервер, как это обычно и бывает в большинстве публичных репозиториев **Github**), например:

```
$ git clone ssh://admin@remote_server_ip:/projects/scripts/bashscripts
```

Чтобы клонировать репозиторий в определенный каталог (**~/bin/bashscripts**), используйте приведенную ниже команду:

```
$ git clone ssh://admin@remote_server_ip:/projects/scripts/bashscripts ~/bin/bashscripts
```

[![Clone-Shared-Git-Repository-to-Local](http://blog.sedicomm.com/wp-content/uploads/2018/10/Clone-Shared-Git-Repository-to-Local.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Clone-Shared-Git-Repository-to-Local.png)

Теперь у вас есть локальный экземпляр проекта в **non\-bare** репозитории (с рабочим каталогом), вы можете создать начальную структуру проекта (Например, добавить файл README.md, подкаталоги для разных категорий скриптов. Или же, переконфигурировать для хранения сценариев reconnaissance и т. д.):

```
$ cd ~/bin/bashscripts/
$ ls -la
```

[![Create-Git-Project-Structure](http://blog.sedicomm.com/wp-content/uploads/2018/10/Create-Git-Project-Structure.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Create-Git-Project-Structure.png)

#### Проверка сводки состояния Git

Чтобы отобразить статус вашего рабочего каталога, используйте команду **status**, которая покажет вам все сделанные вами изменения; какие файлы не отслеживаются **Git**; те изменения, которые были выполнены и так далее.

```
$ git status
```

[![Check-Git-Status](http://blog.sedicomm.com/wp-content/uploads/2018/10/Check-Git-Status.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Check-Git-Status.png)

#### Изменения в Git Stage и Commit

Затем сохраните все изменения, используя команду **add** с флагом **\-A** и выполните начальный коммит. Флаг **\-a** указывает команде автоматически добавлять файлы, которые были изменены, а флаг **\-m** используется для выведения сообщения о выполнения коммита:

```
$ git add -A
$ git commit -a -m "Initial Commit"
```

[![Do-Git-Commit](http://blog.sedicomm.com/wp-content/uploads/2018/10/Do-Git-Commit.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Do-Git-Commit.png)

#### Публикация локальных коммитов в удаленный репозиторий Git

По мере того как команда проекта выполняет поставленную задачу, вы можете пушить (размещать) изменения в центральном репозитории с помощью команды **push**:

```
$ git push origin master
```

[![Push-Commit-to-Centrol-Git-Repository](http://blog.sedicomm.com/wp-content/uploads/2018/10/Push-Commit-to-Centrol-Git-Repository.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Push-Commit-to-Centrol-Git-Repository.png)

Прямо сейчас, ваш локальный репозиторий **git** должен быть синхронизирован с центральным репозиторием проекта, вы можете проверить это, снова запустив команду **status**:

```
$ git status
```

[![Check-Git-Status](http://blog.sedicomm.com/wp-content/uploads/2018/10/Check-Git-Status-1.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Check-Git-Status-1.png)

Вы также можете сообщить своим коллегам, чтобы они начали работу над проектом, клонировав репозиторий на их локальные компьютеры.

#### Создадим новое ветвление в Git

Ветвление (**Branch**) позволяет вам работать с функциями вашего проекта или исправлять проблемы, не трогая основу кода (основную ветку). Чтобы создать новую ветку и затем переключиться на неё, используйте команды **branch** и **checkout** соответственно:

```
$ git branch latest
$ git checkout latest
```

Кроме того, вы можете создать новую ветку и переключиться на нее за один шаг, используя команду **checkout** с флагом **\-b**:

```
$ git checkout -b latest
```

Также, вы можете создать новую ветвь, основанную на другой ветви:

```
$ git checkout -b latest master
```

Чтобы проверить, в какой ветке вы находитесь, используйте команду **branch** (символ звездочки указывает на активную ветку):

```
$ git branch
```

[![Check-Active-Branch](http://blog.sedicomm.com/wp-content/uploads/2018/10/Check-Active-Branch.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Check-Active-Branch.png)

После создания и перехода на новую ветку внесите в неё некоторые изменения и выполните несколько коммитов:

```
$ vim sysadmin/topprocs.sh
$ git status
$ git commit add sysadmin/topprocs.sh
$ git commit -a -m 'modified topprocs.sh'
```

#### Объединение изменений в одной ветке к другой

Чтобы объединить изменения в **ветке\-филиале** в **ветку\-мастер,** переключитесь на главную ветвь и выполните слияние (**merge**):

```
$ git checkout master
$ git merge test
```

[![Merge-Test-Branch-into-Master](http://blog.sedicomm.com/wp-content/uploads/2018/10/Merge-Test-Branch-into-Master.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Merge-Test-Branch-into-Master.png)

Если вам больше не нужна конкретная ветка, вы можете удалить её, используя флаг **\-d**:

```
$ git branch -d test
```

#### Сохранение изменений из удаленного центрального хранилища в локальное

Предполагая, что члены вашей команды внесли изменения в центральный репозиторий проекта, вы можете загрузить любые изменения в свой локальный экземпляр проекта с помощью команды **pull**:

```
$ git pull origin
```

Или же:

```
$ git pull origin master #if you have switched to another branch
```

[![Pull-Changes-from-Central-Repository](http://blog.sedicomm.com/wp-content/uploads/2018/10/Pull-Changes-from-Central-Repository.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Pull-Changes-from-Central-Repository.png)

#### Осмотр репозитория Git и выполнение сравнений

В этом последнем разделе мы расскажем о некоторых полезных функциях **Git**, которые отслеживают все действия, которые произошли в вашем репозитории, что позволяет просматривать историю проекта.

Первой особенностью является **журнал Git**, в котором отображается фиксация изменений:

```
$ git log
```

[![View-Git-Commit-Logs](http://blog.sedicomm.com/wp-content/uploads/2018/10/View-Git-Commit-Logs.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/View-Git-Commit-Logs.png)

Еще одна важная функция — команда **show**, которая отображает различные типы объектов (например, коммиты, теги, деревья и т.д.):

```
$ git show
```

[![Git-Show-Objects](http://blog.sedicomm.com/wp-content/uploads/2018/10/Git-Show-Objects.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Git-Show-Objects.png)

Третьей важной особенностью, которую вам нужно знать, является команда **diff**, используемая для сравнения или отображения разницы между ветвями, отображения изменений между рабочим каталогом и индексом, отображения изменений между двумя файлами на диске и многого другого.

Например, чтобы показать разницу между основной и дочерней ветвью, вы можете выполнить следующую команду:

```
$ git diff master latest
```

[![Show-Difference-Between-Branches](http://blog.sedicomm.com/wp-content/uploads/2018/10/Show-Difference-Between-Branches.png)](http://blog.sedicomm.com/wp-content/uploads/2018/10/Show-Difference-Between-Branches.png)

#### Итоги

**Git** позволяет команде людей работать вместе, используя один и тот же файл(ы), с возможностью просмотра изменений в файле(ах).

Таким образом, вы можете использовать **Git** для управления исходным кодом, конфигурационными файлами или любым файлом, хранящимся на компьютере. Вы можете обратиться к документации [Git Online](https://git-scm.com/doc) для более детального ознакомления.
