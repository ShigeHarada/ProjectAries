Support for ASP.NET Core Identity was added to your project
// ASP.NETコアIDのサポートがプロジェクトに追加されました
- The code for adding Identity to your project was generated under Areas/Identity.
// - アイデンティティをプロジェクトに追加するためのコードは、エリア/アイデンティティの下に生成されました。

Configuration of the Identity related services can be found in the Areas/Identity/IdentityHostingStartup.cs file.
// ID関連サービスの設定は、Areas / Identity / IdentityHostingStartup.csファイルにあります。

The generated UI requires support for static files. To add static files to your app:
// 生成されたUIには、静的ファイルのサポートが必要です。 スタティックファイルをアプリに追加するには：
1. Call app.UseStaticFiles() from your Configure method
// 1.設定メソッドからapp.UseStaticFiles（）を呼び出します。

To use ASP.NET Core Identity you also need to enable authentication. To authentication to your app:
// ASP.NET Core Identityを使用するには、認証を有効にする必要もあります。 アプリを認証するには：
1. Call app.UseAuthentication() from your Configure method (after static files)
// 1.設定メソッド（静的ファイルの後）からapp.UseAuthentication（）を呼び出す

The generated UI requires MVC. To add MVC to your app:
// 生成されたUIにはMVCが必要です。 アプリにMVCを追加するには：
1. Call services.AddMvc() from your ConfigureServices method
// 1. ConfigureServicesメソッドからservices.AddMvc（）を呼び出します。
2. Call app.UseMvc() from your Configure method (after authentication)
// 2.設定メソッド（認証後）からapp.UseMvc（）を呼び出します。

Apps that use ASP.NET Core Identity should also use HTTPS. To enable HTTPS see https://go.microsoft.com/fwlink/?linkid=848054.
// ASP.NET Core Identityを使用するアプリケーションでもHTTPSを使用する必要があります。 HTTPSを有効にするには、https：//go.microsoft.com/fwlink/？linkid = 848054を参照してください。