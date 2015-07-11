[Xamarin] 障礙排除
=

安裝了 **visual studio 2015RC** 後, Xamarin也一起安裝完成了,
就趕緊來試試看,不過沒想到卻是多災多難阿

##障礙1: SDK版本不夠高,無法檢視 (require 23.x.x or higher SDK)
當我開啟 axml檔案並切換到檢視時, layout卻不能顯示!?
看了提示訊息後發現是SDK版本不夠高 (提示訊息就不po了,因為很明顯)

<i class="icon-lightbulb"> **解法**:<i>
二話不說開啟SDK manager進行升級,點選update升級至最新的24.x.x版本

##障礙2: SDK安裝時,拒絕存取
但是更新之路似乎非如此順利,在unpacking的時候,卻出現了**存取被拒**的訊息
<i class="icon-lightbulb"> **解法**:<i>

 - Method 1: 重新開visual studio 但是要用管理者身分開啟就可以安裝了
 - Method 2: 直接去google官方下載新的SDK,然後把整包丟進原本programfile(x86)\android\sdk裡面

##障礙3: SDK版本不穩定,無法檢視
裝完後本來以為就可以順利開啟,沒想到卻出現下列錯誤:
>The layout could not be loaded: The operation failed due to an internal error: com.android.ide.common.rendering.api.SessionParams.

<i class="icon-lightbulb"> **解法**:<i>
查了之後,原因是因為SDK版本不穩,網路上很多都說換V19就可以,
但是我測試後還是不行,最後終於讓我找到一個可以用的版本
<i class="icon-download"> **windows版 SDK**:<i> [Download](https://db.tt/iOmfGADf) 下載之後, 把整個tool資料夾蓋掉原本sdk資料夾中的tool即可

以上就搞定了layout問題了, 謝謝指教!

<i class="icon-book"> **參考連結**:<i>
1. 解決障礙3,提供windows跟mac版的穩定SDK [點我前往](https://forums.xamarin.com/discussion/42333/requires-xamarin-update-android-sdk-tools-rev-24-3)


本篇是採visual studio 2015 RC Xamarin開發, 因此使用Xamarin studio跟Mac的我就不知道該怎麼弄了Orz