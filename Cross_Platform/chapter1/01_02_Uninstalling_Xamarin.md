#ж��Xamarin

`�Ӽ����ж��Xamarin��Ʒ`

��ƪ���½�����δ�һ��Mac��Windows�������ж��Xamarin Studio������Xamarin��Ʒ��


##����
�����кܶ�Xamarin��Ʒ�����������Mac��Windows�����Ͽ�����ƽ̨Ӧ�ó��򡪡���Xamarin Studio��Xamarin.Android��Xamarin.iOS����Mac�ϵ�: Xamarin.Mac��������ĳЩ����±���ж��Xamarin���߼�����ָ�Ͼ���Ϊ����ʵ�����������

�ڱ�ָ�������ǿ��Կ���:

* 1.[ж�� Xamarin Studio](#Uninstall-Xamarin-Studio)
* 2.[ж�� Mono](#Uninstall-Mono-SDK)
* 3.[ж�� Xamarin.Android](#Uninstall-Xamarin-Android)
* 4.[ж�� Xamarin.iOS](#Uninstall-Xamarin-iOS)
* 5.[ж�� Xamarin.Mac](#Uninstall-Xamarin-Mac)
* 6.[��Windowsж�� Xamarin](#Uninstalling-Xamarin-on-Windows)

�������ʹ��ͨ�ð�װ������װXamarin���ڰ�װ֮ǰ�����������������������

##��Mac��ж��Xamarin
��ͨ����������Ӧ���½��˽�ж��ÿ�������Ĳ�Ʒ, �������ϣ����ȫ����Ļ�ж������Xamarin����һ·���������ָ����
Ҫ�˽��й�ʹ��ж�ؽű��İ������������ĵ���ײ���ж�ؽű����֡�

###<a name="Uninstall-Xamarin-Studio"></a>ж��Xamarin Studio
������Mac��ж��Xamarin Studio�ĵ�һ�����Ƕ�λ���� /Applications Ŀ¼�е�Xamarin Studio.app�� �����ϵ���ֽ¨������, ������һ���ѡ���ƶ�����ֽ¨��������ͼ��ʾ��

![](image1.png)

ɾ�����appװ�����Ƴ�Xamarin Studio, Ȼ��, ��������Xamarin��ص��ļ������������ϵͳ��

Ҫɾ��Xamarin Studio�����кۼ�, ���ն�������������:

```shell
sudo rm -rf "/Applications/Xamarin Studio.app��
rm -rf ~/Library/Logs/XamarinStudio-*
rm -rf ~/Library/XamarinStudio-*
```

###<a name="Uninstall-Mono-SDK"></a>ж�� Mono SDK (MDK)
Mono ��һ��Microsoft�� .NET ��ܵĿ�Դʵ�֣���ʹ����Xamarin ���в�Ʒ����Xamarin.iOS,��Xamarin.Android��Xamarin.Mac������������Щƽ̨����C# ������.

> ע��: ��Xamarin���������Ӧ�ó���Ҳʹ��Mono, ��Unity����ɾ��Monoǰ��ȷ��û������������������

Ҫ����Ļ����Ƴ�Mono��ܣ����ն������������

```shell
sudo rm -rf /Library/Frameworks/Mono.framework
sudo pkgutil --forget com.xamarin.mono-MDK.pkg
```

###<a name="Uninstall-Xamarin-Android"></a>ж�� Xamarin.Android
Xamarin.Android ������ʹ��Xamarin Studio���õ�C#����F#����Android����װ��ʹ��Xamarin.Android�����������, ��Android SDK��Java SDK��������[�ֶ���װָ��](#TODO)��ø��������Щ�����������Ϣ��

ʹ�����������Ƴ� Xamarin.Android:

```shell
sudo rm -rf /Developer/MonoDroid
rm -rf ~/Library/MonoAndroid
sudo pkgutil --forget com.xamarin.android.pkg
```

``ж�� Android SDK and Java SDK``
����AndroidӦ�ó�����ҪAndroid SDK���������Ҳ���뿪��Android�������ж��Android SDK: ��λ���� ~/Library/Developer/Xamarin/ ���ļ����Ƴ���������, ����ͼ��ʾ��

![](image2.png)

Java SDK (JDK) ����Ҫж��, ���Ѿ���Mac OS X��Ԥ�õİ���

###<a name="Uninstall-Xamarin-iOS"></a>ж�� Xamarin.iOS
Xamarin.iOS��������Mac�ϵ�Xamarin Studio��ʹ��C#��F#����iOSӦ�ó���Xamarin Build HostҲ�� Xamarin.iOS�Զ���װ����������Visual Studio�п���iOS��Ҫ����Ļ���ж�ض��ߣ������²��裺

1.ʹ�������ն����������ļ�ϵͳ�Ƴ�����Xamarin.iOS �ļ��� 

```shell
rm -rf ~/Library/MonoTouch
rm -rf /Library/Frameworks/Xamarin.iOS.framework   
sudo pkgutil --forget com.xamarin.xamarin-ios-build-host.pkg
``` 

2.ж�� Mac Build Host�������������ն��������Ƴ� Build Host Ӧ�ó���

```shell
rm -rf "/Applications/Xamarin.iOS Build Host.app��
```

3.Build Host ���������������ܻ������л��������ض��Ķ˿ڡ������ͨ�����ն����� launchctl list | grep com.xamarin.mtvs.buildserver �������״̬��

```shell
sudo launchctl unload /Library/LaunchAgents/com.xamarin.mtvs.buildserver.plist
sudo rm -f /Library/LaunchAgents/com.xamarin.mtvs.buildserver.plist
```

###<a name="Uninstall-Xamarin-Mac"></a>ж�� Xamarin.Mac

һ�� Xamarin Studio �ѱ��ɹ�ж�أ�Xamarin.Mac����ʹ�����¶����������Ļ����Ƴ���

```shell
rm -rf /Library/Frameworks/Xamarin.Mac.framework
rm -rf $HOME/Library/Xamarin.Mac
```

###ʹ��ж�ؽű�
���������������������,��Ҫ����ж�ؽű�����Ҫ�����²�����������
1.����ж�ؽű�������������λ�á�Ĭ����������� /Downloads Ŀ¼��
2.���ն˺��л��������ű���Ŀ¼�����룺
```
cd /location/of/file
```
3.���� pwd ���ӡ����Ŀ¼ (���ǵ�ǰ���ڵ��Ǹ�). ��Ӧ���ܹ������ű� xamarin_uninstall.sh
4.���нű�:
./xamarin_uninstall.sh 

��������Xamarin����Ӧ�óɹ������ļ����ɾ����


##<a name="Uninstalling-Xamarin-on-Windows"></a>��Windowsж�� Xamarin 
ͨ�����������Դ�����Windows������ж��Xamarin������������͹��ܣ������ > ж��һ����������ͼ��ʾ��

![](image3.png)

![](image4.png)

Ҫж�� Xamarin Studio���ҵ��ڳ����б��е� Xamarin Studio 5.x.x �͵��ж�ذ�ť��Ҫж��Visual Studio��Xamarin��չ���� SDKs, �ҵ������б��е� Xamarin�͵��ж�ء�������Ľ�ͼ����ʾ:

![](image5.png)

Ҫ��ɾ���ɾ��������һЩ�����Ƴ��ĳ�����������б�

* Android SDK

![](image6.png)

* GTK#

![](image7.png)

* Xamarin Universal Installer

![](image8.png)

* Java SDK (ɾ�����ʱҪС��, ���ܴ�����������������)

![](image9.png)


##С��
�ڱ������ǿ���ͨ��ʹ���ն�������ȫ�����Macж��Xamarin��Ҳͨ������͹���ѡ������Windows������ж��Xamarin��
