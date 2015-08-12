#�ƶ��������

�����ƶ�Ӧ�ó������������IDEһ����, һ�𶪵㶫��, ��һ����ٲ���, ���ύ��һ��App�̵� ���� ���е���һ��������ɡ�������������һ���ǳ����ӵĹ��̣������ϸ��Ԥ�����, �����Բ���, ��ǧ������豸�ϵ�QA����, һ�������� beta ��������, ��Ȼ�����Ĳ���ʽ��

�ڱ��ĵ�, ���ǽ�Ҫȫ�������ι���һ��Xamarin�ƶ�Ӧ�ó���, ������
1.[����](#Requirements) �C ���ǻ�ö�ٺ���鹹��iOS��AndroidӦ�ó�������� 
2.[Xamarin���](#Xamarin) �C Xamarinƽ̨�����б� 
3.[Xamarin��ι���?](#How-Does-Xamarin-Work) �C Xamarin��C#����iOS��Android����ԭ��ļ�Ҫ������ 
4.[����!](#Getting-Started) �C ��iOS, Android, ��ʹ��Xamarin.Forms������ƽ̨�ϣ��������ĵ�һ��XamarinӦ�ó��� 

����ּ�ڽ���Xamarinƽ̨��Ҫ�˽������ڹ����ƶ�Ӧ�ó��򣬴���Ƶ����ԵĹ���, ����[�ƶ�Ӧ�ÿ����������ڼ��](05_Introduction_to_the_Mobile_SDLC.md) �ĵ���

##<a name="Requirements"></a>����
������뿪��iOS, ����������Xamarin Studio��Visual Studio�б�д����, ����ͷ�ϱ�����һ̨װ������OS X Mountain Lionϵͳ��ƻ��MAC���ԡ���ȻXamarinӦ�ó������.NET BCL����C#��д,Xamarin����ҪiOS SDK��Xcode�Ա���롣����, iOS�豸ģ���������iOS SDK��һ����, ���ֻ����Mac�ϡ�Ϊ������iOS SDK, �������[Apple�����߱�̻�Ա](http://developer.apple.com/)�������Ա��Ҫ������Ա��ÿ��$99����

������ܵ����н̳��ǻ������µİ汾����װ����һ�̳��н���.

##<a name="Xamarin"></a>Xamarin���
�ڿ�����ι���iOS��AndroidӦ�ó���ʱ���������Ϊԭ��������, Objective-C��Java, �ֱ��ǽ��е�ѡ�񡣲����������ڹ�ȥ�ļ�����, �������µ�����ƽ̨����̬ϵͳ�������ƶ�Ӧ�ó���

Xamarin������ط����ص���ͨ���ṩһ����һ������ �C C#, ���, �������ڿ����������ƶ�ƽ̨:iOS, Android,��Windows Phone (Windows Phone��ԭ�����Ծ���C#), ͬʱ������ԭ�� (�ǽ����͵�) Ӧ�ó���������������������̵���Ϸ��

ÿ��ƽ̨���в�ͬ�Ĺ��ܼ�������ÿ�ֲ�ͬ�ĵط������԰�ԭ��������дӦ�ó��� �C Ҳ����˵, ����Ϊ���������Ӧ�ó�����ײ�Java��ϵͳ����������������, ĳЩƽ̨��ֻ��������HTML��JavaScript����Ӧ�ó���, ��һЩ�ǳ��ͼ���ֻ����C/C++���롣����ĳЩƽ̨�ϲ����ñ����ؼ����߰���

Xamarin�Ƕ��صģ�����������е�ԭ��ƽ̨����������������һЩǿ����Լ����ص�, ������

* 1.�����ԭ��SDKs �C Xamarin����������������ƽ̨ SDKs�İ󶨣�����iOS��Android.������, ��Щ����ǿ���͵ģ�����ζ�����Ǻ����������ʹ��, ���ṩ�ڱ���ʱ�Ϳ����ڼ�ǿ������ͼ�顣�⵼������ʱ������ٺ͸���������Ӧ�á�
* 2.Objective-C, Java, C, �� C++ ������ �C Xamarin �ṩ����ֱ�ӵ��� Objective-C, Java, C, �� C++ �Ŀ�, ����ʹ�ô����Ѿ������ĵ��������������������������������е���Objective-C, Java ��C/C++��д��iOS��Android�⡣����, Xamarin�ṩ����Ŀ�����������ɰ�ԭ��Objective-C �� Java ��ʹ���������﷨�� 
* 3.�ִ����Թ��� �C Xamarin Ӧ�ó�����C#��д, һ���ִ����ԣ�������Objective-C��Java���ش�Ľ��綯̬��������, ����ʽ������lambda, LINQ , ���б������, ���ӵķ��͵ȵȡ� 
* 4.���˵Ļ���� (BCL) �C Xamarin Ӧ�ó���ʹ�� .NET BCL, һ���޴���༯�ϣ��������ۺϺ��Ż����ܣ���ǿ���XML, ���ݿ�, ���л�, IO, �ַ���, ������֧��, ������ЩΪ��������, ���е� C# �����ܱ��뵽���Ӧ�ó�����ʹ��, ���ṩ�˷��ʳ�ǧ����Ŀ⣬�����������Ķ����Ѿ�������BCL�ϡ� 
* 5.�ִ����ɿ������� (IDE) �C Xamarin �� Mac OS X��ʹ��Xamarin Studio , ��Windows��ʹ��Xamarin Studio �� Visual Studio 2013����Щ�����ִ� IDE������������������Զ����, һ�����ӵ���Ŀ�ͽ����������ϵͳ, һ��ȫ�����Ŀģ���, ����Դ��������ȵȡ� 
* 6.�ֻ���ƽ̨֧�� �C Xamarin �����ƶ�ƽ̨���ṩ���ӵĿ�ƽ̨֧��iOS��Android��Windows�ֻ���Ӧ�ó�����Թ����д����90%�Ĵ���, �������ǵ�Xamarin.Mobile������������ƽ̨�ṩһ��ͳһ��API�����ʹ�����Դ��������г�ΪĿ������������е��ƶ�ƽ̨���ƶ�������Ա�������������Ϳ����ɱ���ʱ�䡣

����Xamarin��ǿ���ȫ��Ĺ��ܼ�, Ӧ�ó��򿪷���Աϣ��ʹ��һ���ִ����Ժ�ƽ̨������ƽ̨�ֻ�Ӧ�ó��������һ��հס�

ע��:

������ϵ�е��ص��ǿ�ʼ����iOS��AndroidӦ�ó��� ������Թ���Windows Phone����Ȥ, Microsoft �ṩ�̳���[��](http://dev.windowsphone.com/en-us/develop)�� �������Ҫ�˽�������et Xamarin��ƽ̨���� (���� Windows Phone), �������[����](http://developer.xamarin.com/guides/ios/application_fundamentals/building_cross_platform_applications)�ҵ�ָ�ϡ�

����������������Ĺ���ԭ��


##<a name="How-Does-Xamarin-Work"></a>Xamarin��ι���?
Xamarin �ṩ��������ҵ��Ʒ: Xamarin.iOS �� Xamarin.Android�����Ƕ�������Mono֮��, һ������.NET��ܵĿ�Դ�汾�����ѷ�����.NET ECMA ���Mono�Ѿ����ڲ��һ.NET�������һ����, ���ڼ����κ�ƽ̨�����У�����Linux, Unix, FreeBSD, �� Mac OS X.

��iOS, Xamarin�� Ahead-of-Time ( AOT) ������ֱ�ӱ��� Xamarin.iOS Ӧ�ó���ԭ�� ARM �����롣�� Android, Xamarin�ı��������뵽�м����� ( IL), Ȼ���ǵ�Ӧ�ó�������ʱ��Just-in-Time ( JIT) ����Ϊ�������򼯡�

����Щ�����, Xamarin Ӧ�ó�����������ʱ�Զ�����һЩ���飬���ڴ����, �����ռ�, �ײ�ƽ̨������,�ȵȡ�

###MonoTouch.dll �� Mono.Android.dll
Xamarin Ӧ�ó��򹹽������.NET BCL���Ӽ�����ΪXamarin �ƶ����á��������ļ��Ѿ�������ר��Ϊ�ƶ�Ӧ�ó���Ͱ�װMonoTouch.dll �� Mono.Android.dll (�ֱ�ΪiOS��Android)������� Silverlight (�� Moonlight) Ӧ�ó����ǹ�������� Silverlight/Moonlight .NET ���õķ�ʽ��ʵ����, Xamarin �ƶ������ļ��൱�� Silverlight 4.0 ���ú��������һ��BCL�ࡣ

�йؿ��ó��򼯺���������б�, ���� [Xamarin.iOS](http://developer.xamarin.com/guides/ios/advanced_topics/assemblies) ����� [Xamarin.Android](http://developer.xamarin.com/guides/android/advanced_topics/assemblies) ����

���� BCL, ��Щ .dlls ������������ iOS SDK �� Android SDK ��װ��������ֱ�Ӵ�C#���õײ� SDK APIs��

###Ӧ�ó������
�� Xamarin Ӧ�ó��򱻱���, �����һ��Ӧ�ó����, Ҫô����iOS�е�һ�� .app �ļ�, Ҫô����Android�е�һ�� .apk �ļ�����Щ�ļ���ԭ��Ӧ�ó����û��ʲô���𣬲�����ͬ����ʽ����


##<a name="Getting-Started"></a>����
�������Ѿ��˽�Xamarin����ι�����, ��ʱ�򿪸���!

��һ����ʹ����Щָ��֮һ����ʼ������һ��Ӧ��:

* [Hello, iOS](http://developer.xamarin.com/guides/ios/getting_started/hello%2c_world)

![](ios.png)

* [Hello, Android](http://developer.xamarin.com/guides/android/getting_started/hello%2c_world)

![](android.png)

* [Xamarin.Forms���](http://developer.xamarin.com/guides/cross-platform/xamarin-forms/introduction-to-xamarin-forms/)

##С��
����ֻ�ǽ�����Xamarinƽ̨������õ����Ӧ�ó�������ʱ����������Ȥ�ſ�ʼ����� ``Hello, iOS``, ``Hello, Android``, �� ``Xamarin.Forms���`` ָ���Կ�ʼ��