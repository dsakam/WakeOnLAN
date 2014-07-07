WakeOnLAN
=========

Wake on LAN PowerShell Script Version **1.0.0.0**

概要
----
Wake on Lan を実行する GUI 付きの PowerShell スクリプトです。

PackageBuilder モジュールの `Show-InputBox` コマンドレットを使用するため、PackageBuilder モジュールがインポートされている必要があります。  
PackageBuilder モジュールがインポートされていない場合は、最初に PackageBuilder モジュールのインポートを試みます。
失敗した場合は、例外をスローして終了します。

通常、テキスト ボックス付きのメッセージ ボックスが表示され、MAC アドレスを指定することで対象のコンピューターを起動しますが、下記のファイルが存在し、かつ、そのフォーマットで適切であった場合は、コンボ ボックスが表示されます。

    %HOMEDRIVE%%HOMEPATH%\Documents\WindowsPowerShell\Modules\PackageBuilder\mac-addresses

または

    $env:HOMEDRIVE | Join-Path -ChildPath $env:HOMEPATH `
     | Join-Path -ChildPath \Documents\WindowsPowerShell\Modules `
     | Join-Path -ChildPath \PackageBuilder\mac-addresses

このファイルのフォーマットは下記ように、各行に表示名と MAC アドレスをタブ文字で区切ります。

    PC1   00:00:00:00:00:00:00:AA
    PC2   00:00:00:00:00:00:00:FF

履歴
----

**Version 1.0.0.0** (2014/07/07)
1st Edition
