ポイント対サイトで VNet に接続するすべてのクライアント コンピューターには、クライアント証明書がインストールされている必要があります。 クライアント証明書はルート証明書から生成され、各クライアント コンピューターにインストールされます。 有効なクライアント証明書がインストールされていない状態でクライアントが VNet に接続した場合、認証に失敗します。

クライアントごとに一意の証明書を生成することも、複数のクライアントに同じ証明書を使用することもできます。 一意のクライアント証明書を生成する利点は、1 つの証明書を失効させることができる点です。 そうでなければ、複数のクライアントが同じクライアント証明書を使用していて、その証明書を失効させる必要がある場合は、認証にその証明書を使用するすべてのクライアントに新しい証明書を生成してインストールする必要があります。

クライアント証明書は、次の方法で生成できます。

- **エンタープライズ証明書:**

  - エンタープライズ証明書ソリューションを使用している場合は、"domain name\username" 形式ではなく、共通名の値の形式 "name@yourdomain.com" を使用してクライアント証明書を生成します。
  - クライアント証明書が、使用リストの最初の項目としてスマート カード ログオンなどではなく "クライアント認証" が指定されている "ユーザー" 証明書テンプレートに基づいていることを確認します。証明書を確認するには、クライアント証明書をダブルクリックし、*[詳細]、[拡張キー使用法]* の順に選択して表示します。

- **自己署名ルート証明書:** [ポイント対サイト接続の自己署名ルート証明書の作成](../articles/vpn-gateway/vpn-gateway-certificates-point-to-site.md#clientcert)に関する記事の手順で自己署名ルート証明書からクライアント証明書を生成した場合、その作業に使用したコンピューターに自動的にクライアント証明書がインストールされます。 クライアント証明書を別のクライアント コンピューターにインストールする場合は、その証明書をエクスポートする必要があります。 [クライアント証明書のエクスポート](../articles/vpn-gateway/vpn-gateway-certificates-point-to-site.md#clientexport)に関する記事の手順に従ってください。