### <a name="serialport-background-thread-exceptions"></a>SerialPort バックグラウンド スレッドの例外

|   |   |
|---|---|
|説明|OS 例外がスローされたとき、<xref:System.IO.Ports.SerialPort> ストリームで作成されたバックグラウンド スレッドによってプロセスが終了することがなくなりました。 .NET Framework 4.7 以前のバージョンを対象とするアプリケーションでは、<xref:System.IO.Ports.SerialPort> ストリームで作成されたバックグラウンド スレッドでオペレーティング システムの例外がスローされたとき、プロセスが終了になります。 .NET Framework 4.7.1 以降のバージョンを対象とするアプリケーションでは、バックグラウンド スレッドは、アクティブ シリアル ポートに関連付けられている OS イベントを待ち、シリアル ポートが突然取り除かれるなどの場合、クラッシュすることがあります。|
|提案される解決策|.NET Framework 4.7.1 を対象とするアプリケーションの場合、例外処理が望ましくないときは、<code>app.config</code> ファイルの <code>&lt;runtime&gt;</code> セクションに次を追加することで例外処理を無効にできます。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>以前のバージョンの .NET Framework を対象とするが、.NET Framework 4.7.1 以降で実行するアプリの場合、<code>app.config</code> ファイルの <code>&lt;runtime&gt;</code> セクションに次を追加することで例外処理を選択できます。<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|スコープ|マイナー|
|Version|4.7.1|
|型|再ターゲット中|
|影響を受ける API|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|
