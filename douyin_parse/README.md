# douyin_parse
参考：https://github.com/DLWangSan/douyin_parse</br>
增加了批量下载</br>
下载视频所在douyin_download(自动创建)</br>
后期会再修改</br>
</br>
2020/04/06</br>
审查元素 例：</br>
默认抖音视频分享的链接(短链接)：</br>
https://v.douyin.com/WuRMPV
</br>
访问跳转至：</br>
https://www.iesdouyin.com/share/video/6805024822687534344/?region=CN&mid=6805019515144391427&u_code=13248lk0l&titleType=title&utm_source=copy_link&utm_campaign=client_share&utm_medium=android&app=aweme
</br>
删去后面的部分参数依然可以访问：</br>
https://www.iesdouyin.com/share/video/6805024822687534344/?region=CN&mid
</br>
打开浏览器审查元素，并点击播放，得到一个水印视频的地址：</br>
https://aweme.snssdk.com/aweme/v1/playwm/?s_vid=93f1b41336a8b7a442dbf1c29c6bbc561699c13ffb2ce3cacb960e9bcb7c0b8f9f0ec410108d165bd0bfd2b83c1070676ccafc940fd5dc933ea73704a90e4faf&line=0
</br>
以及封面：</br>
https://p3.pstatp.com/large/tos-cn-p-0015/584d6a06932940998a1decc057ab2978_1584418313.jpg
</br>
访问第一个获取的水印地址，跳转至：</br>
http://v6-dy-y.ixigua.com/d3bcbb96ea87f77cefcdee819c7a2dfb/5e8b5486/video/tos/hxsy/tos-hxsy-ve-0015/832e6e52408d4c1e931b763b152e5d21/?a=1128&br=0&bt=2405&cr=0&cs=0&dr=0&ds=3&er=&l=2020040623103601000806423716CB0748&lr=aweme&qs=0&rc=am9oczx5OzQ3czMzZGkzM0ApODVpNzk8OWRmNzVnM2g1N2dsZTFhci9fcGxfLS1fLS9zczM0Yl8vMzVfYGBhNmItYTE6Yw%3D%3D&vl=&vr=
</br>
获得去水印视频地址很简单，把水印地址中playwm改成play：</br>
https://aweme.snssdk.com/aweme/v1/play/?s_vid=93f1b41336a8b7a442dbf1c29c6bbc561699c13ffb2ce3cacb960e9bcb7c0b8f9f0ec410108d165bd0bfd2b83c1070676ccafc940fd5dc933ea73704a90e4faf&line=0</br>
访问需要将浏览器修改成手机(建议Chrome)</br>
http://v1-dy.ixigua.com/ea0d435d7fd297dec60bb2dfe0304ffb/5e8b550c/video/tos/hxsy/tos-hxsy-ve-0015/a1b16da401e24addad7680d1b6646659/?a=1128&br=0&bt=1561&cr=0&cs=0&dr=0&ds=6&er=&l=2020040623125001001901703525C7D635&lr=&qs=0&rc=am9oczx5OzQ3czMzZGkzM0ApNmhlZmRoaWQ1N2U3OWlpNWdsZTFhci9fcGxfLS1fLS9zc2BeMTVhYl5fLzIuYmFiLTM6Yw%3D%3D&vl=&vr=
</br>
http://v6-dy.ixigua.com/5661367ade39e41401b8692f896fee61/5e8b55d7/video/tos/hxsy/tos-hxsy-ve-0015/a1b16da401e24addad7680d1b6646659/?a=1128&br=0&bt=1561&cr=0&cs=0&dr=0&ds=6&er=&l=202004062316130100120341581AD3539A&lr=&qs=0&rc=am9oczx5OzQ3czMzZGkzM0ApNmhlZmRoaWQ1N2U3OWlpNWdsZTFhci9fcGxfLS1fLS9zc2BeMTVhYl5fLzIuYmFiLTM6Yw%3D%3D&vl=&vr=
</br>
发现有多个地址(流)
</br></br>
分析网站，有点看不懂：</br>
iesdouyin.com：跳转抖音官网</br>
snssdk.com：跳转今日头条APP下载页面</br>
pstatp.com：nginx</br>
ixigua.com：跳转西瓜视频</br>