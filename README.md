<h1>perf-orange-cat</h1>
<br/>
<h1>客户端性能测试平台 https://github.com/1033866383/perf-orange-cat/releases/download/v1.0.0/perf-orange-cat.zip</h1>

![微信图片_20230624120931](https://github.com/1033866383/perf-orange-cat/assets/56209295/ce1d47eb-01bb-41d8-88d4-e07828aea825)

<h2>演示地址：http://112.126.75.188/</h2>

<h2>简介</h2>
<ul>
    <li>替代perfdog等客户端性能测试工具</li>
    <li>支持Android/IOS平台上应用的性能数据测试，包含游戏和视频类app的性能测试</li>
    <li>支持指标包含:cpu,memory,fps,gpu,温度,电量，以及他们的最大值，最小值，平均值</li>
    <li>fps指标中包含：，卡顿（jank），强卡顿（big jank），卡顿率等指标,等指标</li>
    <li>数据结果准确，与perfdog一致</li>
    <li>可用实时记录设备画面，点击图片或者点击图标上的点可用跳转到对对应的场景。</li>
    <li>支持局域网内使用，此平台部署服务后整个局域网访问服务页面就可以直接对本机设备进行性能测试</li>
    <li>提供可执行文件直接执行部署即可，提供api详情</li>
</ul>

<h2>目录介绍</h2>
<ul>
<li>test_result/ 包含前端页面和测试结果。</li>
<li>log.log 为项目运行日志。</li>
<li>task.sqlite 为sqllite数据库，包含了每个任务的基本详情也是唯一的dao对象。</li>
<li>其他可执行文件为不同平台的可执行文件。</li>
</ul>

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/852cda82-058b-4832-9daf-8074c1a7bb6b)

<h2>使用教程</h2>
1.运行exe， Pyinstaller打包的项目首次启动时可能会稍微慢一点。

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/fc99180b-1e26-47e4-87a6-cc3db7d9b9e8)

2.此时项目已经启动了。

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/baae938d-bf01-4f3b-a5e6-0309a718cf2d)

3.访问http://localhost/。

默认页面：

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/100c40ee-499f-437f-8f98-e4469f946e6e)

4.点击上方红色按钮，创建新的性能测试任务。此时会开始自动检测你电脑上连接到Android/Ios设备。
<h3>需要注意的点：Android设备需要打开开发者模式，部分设备可能需要选择传输模式为传输文件！</h3>

<h3>IOS设备IOS系统16版本以上需要在设备上打开开发者选择，在隐私与安全中如下图。设备上如果看不到这个选项可用下载icarefone打开开发者模式。IOS16版本以下的需要连接xcode打开开发者选项。实际上连接一下选中手机就可以了。IOS16也可用通过此操作让开发者选项展示出来，如果是windows电脑连接IOS设备还需要记得安装 iTunes</h3>

![微信图片_20230625011358](https://github.com/1033866383/perf-orange-cat/assets/56209295/78d05b9e-7370-486c-b8cd-3ad0afaf5744)


下面是手机打开开发者选项后检测到的一个Android的模拟器和我自己的iphone手机实例：

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/78634fab-7225-4226-bca1-fdd4884abaec)

5.下拉选中应用，选中后会自动展示版本号，随后点击创建任务。

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/ffbb3ef7-0623-44fd-97a2-f9e17135173b)

6.点击完创建任务后页面会自动刷新，并开始性能测试，如果打开实时显示屏幕按钮，则上方的图片会实时展示手机屏幕的情况。左侧的是时间按钮是此任务的开始时间也代表此任务的名称，IOS的fps下方的卡顿，强卡顿并不会计算，Android则会真实计算，计算方式与perfdog一致。

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/c55b46c6-3903-421a-a9a2-9caf1366f0f7)

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/6de2339e-59a5-4978-9730-007d015154e1)

7.最后点击停止任务，任务即可停止，任务停止之后可用删除任务，删除任务是物理删除会把所有的任务数据删除谨慎删除。

![image](https://github.com/1033866383/perf-orange-cat/assets/56209295/a2f65fca-2256-4fac-a1a3-79fb8899ea0f)


IOS性能测试使用的是tidevice工具：https://github.com/alibaba/taobao-iphone-device
