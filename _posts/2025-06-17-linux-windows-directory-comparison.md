## LinuxとWindowsのディレクトリ対応表

* 自分がいるやつだけ

| Linux | Windows | 説明 |
| :- | :- | :- |
| /bin | C:¥Windows¥System32 | 基本的な実行ファイルを置く |
| /sbin | - | システム管理用の実行ファイル（管理者のみ実行）を格納 |
| /etc | - | システム全体の設定ファイル(テキスト形式)をまとめたディレクトリ。Windowsには統一された設定用フォルダは存在せず、設定はレジストリや各プログラムごと(C:¥WindowsやC:¥ProgramDataなど) |
| /lib | C:¥Windows¥System32` 等 | システムやアプリが利用する共有ライブラリ`.so`を格納。Windowsでは動的ライブラリ(DLL)は主に`System32`や各アプリのインストール先フォルダ |
| /opt | C:¥Program Files | オプション(追加)ソフトウェアをインストールするディレクトリ。Windowsでは通常、サードパーティ製アプリケーションはProgram FilesまたはProgram Files (x86) |
| /tmp | C:¥Windows¥Temp や %TEMP% | 一時ファイル用。WindowsではC:¥Windows¥Temp |
| /usr | - | OS付属のプログラムや追加インストールされたソフトのファイル郡を収める階層ディレクトリ。Windowsは明確な対応なし |
| /var | - | ログやスプールなど可変データを保存するディレクトリ。Windowsでは専用フォルダなし |
| ‾ | %USERPROFILE% | 個人データ保管場所 |
| ‾/Public | %USERPROFILE%\Public | 公開用フォルダ（全ユーザーと共有） |
| ~/.configほか | %LOCALAPPDATA%\Roaming | ユーザー設定・アプリデータ、ユーザー毎のアプリ設定ファイル類)。ユーザープロファイルが異なるPC間を持ち運べるようなデータを配置。Windowsドメイン環境では、Roamingフォルダがサーバーに同期され、任意のPCログオン時に同じ設定が適用される(ローミングプロファイル) |
| ~/.local/share | %LOCALAPPDATA%\Local | 大容量データやキャッシュ等、PC内限定のユーザーデータ |
| ~/.cache | %LOCALAPPDATA%\LocalLow | 権限の低い（サンドボックス化された）アプリ書込領域 |
| ~/bin | %LOCALAPPDATA%\Programs、%USERPROFILE%\bin等を作成し管理 | ユーザー専用の実行ファイル。PATHに含まれる。 %USERPROFILE%\binはPATHへの追加が必要 |
| ~/var | - | - |
| ~/lib | - | - |
| ~/opt | %LOCALAPPDATA%\Programs\&lt;アプリ名&gt; | ユーザーが追加でインストールしたソフトウェア用フォルダ |
| ~/tmp | %TEMP% | ユーザーごとの一時フォルダ。例;C:\Users\&lt;ユーザー&gt;\AppData\Local\Temp |
| | | |
