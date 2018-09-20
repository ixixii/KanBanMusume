# KanBanMusume
WordPress添加看板娘


WordPress博客添加看板娘(送37套服饰)
1.  从我的github下载压缩包

2. 将下载的压缩包 上传到网站的根目录,并解压

scp live2d_v1.0.zip root@xx.xx.xx.xx:/usr/local/nginx/html/vwhm_net_wwwroot/

3. 在header文件中添加以下代码

cd wp-content/themes/twentyseventeen/

<link rel="stylesheet" href="/live2d/css/live2d.css" />
<script type="text/javascript" src="http://apps.bdimg.com/libs/jquery/2.1.4/jquery.js"></script>

4. 在footer文件中body结束标签之前,添加以下代码

<div id="landlord">
    <div class="message" style="opacity:0"></div>
    <canvas id="live2d" width="280" height="250" class="live2d"></canvas>
    <div class="hide-button">隐藏</div>
    <div class="switch-button">换装</div>
</div>

<script type="text/javascript">
    var message_Path = '/live2d/'
    var home_Path = 'http://vwhm.net'  //此处修改为你的域名，必须带斜杠
</script>
<script type="text/javascript" src="/live2d/js/live2d.js"></script>
<script type="text/javascript" src="/live2d/js/message.js"></script>
<script type="text/javascript">
    var index = Math.ceil(Math.random()*37)
        console.log('未闻花名vwhm.net + ' + index)
        loadlive2d("live2d", "/live2d/model/pio/model_"+index+".json");
</script>

​

效果如下:


WordPress博客添加看板娘(送37套服饰)
​

​

