---
title: InfoPath, chiffrement RPC et services Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Les services Web peuvent exposer un style parmi deux pour lier leurs méthodes Web dans le contrat WSDL (Web Service Description Language) qui les décrit : Document ou RPC.'
ms.openlocfilehash: 0eacf013c9cdf74f18f3de1d4412ca4ca165a960
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387677"
---
# <a name="infopath-rpc-encoding-and-web-services"></a>InfoPath, chiffrement RPC et services Web

Les services Web peuvent exposer un style parmi deux pour lier leurs méthodes Web dans le contrat WSDL (Web Service Description Language) qui les décrit : Document ou RPC. En outre, chacun de ces deux styles de liaison peut être spécifié en tant que littéral ou codé. Les implémentations les plus courantes pour chaque type sont : document/littéral et RPC/codé. Cependant, Microsoft InfoPath prend en charge seulement la connexion à des services Web utilisant le style document/littéral.
  
La plupart des outils de développement de services Web permettent de choisir le type de service Web que vous voulez créer. Si vous développez un service Web auquel vous vous connecterez depuis InfoPath, vous devez spécifier document/littéral pour le style et le codage de ce service.
  
Cependant, si vous ne contrôlez pas le service Web que vous voulez utiliser et que vous devez vous connecter à un service Web utilisant le style RPC/codé, vous pouvez utiliser un service de proxy .NET pour vous y connecter.
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a>Utilisation d'un service de proxy .NET pour se connecter à un service Web

Si vous ne contrôlez pas le service Web RPC/codé que vous voulez utiliser, vous pouvez créer un service Web de proxy Microsoft .NET de type document/littéral qui fournit des fonctions de wrapper pour chacune des méthodes Web que vous voulez appeler depuis le service Web RPC/codé. Vous pouvez ensuite utiliser le service Web de proxy document/littéral depuis InfoPath.
  
Le code .NET Framework peut fonctionner avec tous les types de services Web (RPC/codé et document/littéral), et tous les services Web .NET utilisent le style et le codage document/littéral. .NET Framework pouvant communiquer avec tous les types de services Web, vous pouvez créer un service Web .NET qui a des méthodes effectuant des appels au service Web RPC/codé. Le service Web .NET agira en tant que traducteur, permettant à InfoPath d'effectuer des appels de style document/littéral au service Web .NET, qui à son tour peut effectuer des appels de style RPC/codé au service Web d'origine.
  
Les préalables à la création d'un tel service de proxy Microsoft .NET Web sont un ordinateur Microsoft Windows ou Microsoft Windows Server exécutant les services Internet (IIS) avec ASP.NET installé, sur lequel le service Web de proxy peut être déployé. Lorsque vous créez une solution InfoPath, vous pointez vers le service Web de proxy au lieu du service Web RPC/codé. Le service Web de proxy effectue alors des appels au service RPC/codé.
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a>Création d'un service Web de proxy à l'aide de Visual Studio

1. Créez un nouveau projet **Application de service Web ASP.NET**. 
    
2. Dans l' **Explorateur de solutions**, cliquez avec le bouton droit sur le dossier **Références** de votre nouveau projet, puis cliquez sur **Ajouter une référence Web**. 
    
3. Dans la boîte de dialogue **Ajouter une référence Web**, entrez l'URL du service Web RPC/codé que vous voulez utiliser, puis cliquez sur **Aller à**.
    
4. Cliquez sur **Ajouter une référence**. 
    
5. Ouvrez le fichier .asmx pour votre service Web et ajoutez une méthode de service Web pour appeler chaque méthode de service Web depuis le service Web RPC/codé référencé.
    
6. Pour afficher une liste des méthodes dans le serveur Web RPC/codé de référence, affichez la fenêtre **Affichage de classes**. Pour chaque méthode de service Web, vous voyez trois méthodes. Par exemple, si la méthode de service Web est appelée  `doSearch`, vous voyez trois méthodes appelées  `doSearch`,  `BegindoSearch` et  `EnddoSearch`. Vous devez créer un service Web de wrapper seulement pour la méthode  `doSearch`. Vérifiez que vous utilisez exactement la signature et le type de retour de la méthode. 
    
7. Dans chaque méthode de wrapper, vous devez écrire du code pour effectuer un appel au service Web RPC/codé référencé, comme dans l'exemple suivant. 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. Si le service Web RPC/codé requiert une authentification, vous pouvez coder en dur les informations d'identification requises pour la connexion au service Web RPC/codé dans le code source pour le service Web .NET de proxy ou bien vous pouvez utiliser du code similaire à l'exemple suivant. 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

Pour plus d'informations, recherchez l'article de la Base de connaissances Microsoft « Procédure : passage des informations d'identification actuelles à un service Web ASP.NET » (éventuellement en anglais) sur https://support.microsoft.com/.
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a>Création d'un service Web de proxy sans Visual Studio .NET

Il est également possible de créer un service Web de proxy à l'aide des outils fournis avec le Kit de développement logiciel (SDK) .NET Framework, qui peut être téléchargé sur MSDN.
  
Utilisez l'outil Web Services Description Language (Wsdl.exe) pour créer le fichier de code pour votre service Web de proxy. Ce fichier de code peut être compilé à l'aide du compilateur en ligne de commande C# (csc.exe) ou du compilateur en ligne de commande Visual Basic .NET (vbc.exe), qui font également partie du SDK .NET Framework. Après que l'outil Web Services Description Language a généré le fichier de code, renommez l'extension du nom de fichier en .asmx et ouvrez le fichier dans un éditeur de texte. Sur la toute première ligne du document, ajoutez la directive de page suivante :
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

Allez à la fin du fichier de code et créez un appel à chacune des méthodes de service Web du service Web RPC/codé. L'exemple de code suivant montre le code pour un service Web .NET qui se connecte au service Web Google, qui utilise le style de développement RPC/codé. Il y a un espace réservé pour le code généré par wsdl.exe.
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
 
using System; 
using System.Web.Services; 
 
// The auto-generated code from the wsdl.exe tool goes here. 
 
[WebService] 
public class GoogleSearchServiceWrapper : System.Web.Services.WebService  
{ 
    [WebMethod] 
    public System.Byte[] doGetCachedPage(System.String key, System.String url) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doGetCachedPage(key, url); 
    } 
 
    [WebMethod] 
    public System.String doSpellingSuggestion(System.String key, System.String phrase) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doSpellingSuggestion(key, phrase); 
    } 
 
    [WebMethod] 
    public GoogleSearchResult doGoogleSearch(System.String key, 
      System.String q, 
      System.Int32 start, 
      System.Int32 maxResults, 
      System.Boolean filter, 
      System.String restrict, 
      System.Boolean safeSearch, 
      System.String lr, 
      System.String ie, 
      System.String oe) 
    {
        GoogleSearchService srch = new GoogleSearchService();
           return srch.doGoogleSearch(key, q, start, maxResults, 
               filter, restrict, safeSearch, lr, ie, oe); 
    } 
}
```


