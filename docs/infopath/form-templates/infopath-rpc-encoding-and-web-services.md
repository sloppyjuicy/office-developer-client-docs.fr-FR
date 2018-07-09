---
title: InfoPath, chiffrement RPC et services Web
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: 'Les services Web peuvent exposer un style parmi deux pour lier leurs méthodes Web dans le contrat WSDL (Web Service Description Language) qui les décrit : Document ou RPC.'
ms.openlocfilehash: 01b75df42bce97d62ebb5e273588cb522e5e2a09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782383"
---
# <a name="infopath-rpc-encoding-and-web-services"></a><span data-ttu-id="2dd8a-103">InfoPath, chiffrement RPC et services Web</span><span class="sxs-lookup"><span data-stu-id="2dd8a-103">InfoPath, RPC Encoding and Web Services</span></span>

<span data-ttu-id="2dd8a-p101">Les services Web peuvent exposer un style parmi deux pour lier leurs méthodes Web dans le contrat WSDL (Web Service Description Language) qui les décrit : Document ou RPC. En outre, chacun de ces deux styles de liaison peut être spécifié en tant que littéral ou codé. Les implémentations les plus courantes pour chaque type sont : document/littéral et RPC/codé. Cependant, Microsoft InfoPath prend en charge seulement la connexion à des services Web utilisant le style document/littéral.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-p101">Web services can expose one of two styles for binding to their Web methods in the Web Service Description Language (WSDL) contract that describes them: Document or RPC. Additionally, each of these two styles of binding can be specified as either literal or encoded. The most common implementations for each type are: document/literal and RPC/encoded. However, Microsoft InfoPath only supports connecting to Web services that use the document/literal style.</span></span>
  
<span data-ttu-id="2dd8a-p102">La plupart des outils de développement de services Web permettent de choisir le type de service Web que vous voulez créer. Si vous développez un service Web auquel vous vous connecterez depuis InfoPath, vous devez spécifier document/littéral pour le style et le codage de ce service.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-p102">Most Web service development tools provide a switch for specifying what kind of Web service that you want to create. If you are developing a Web service that you will be connecting to from InfoPath, you should specify document/literal as your Web service's style and encoding.</span></span>
  
<span data-ttu-id="2dd8a-110">Cependant, si vous ne contrôlez pas le service Web que vous voulez utiliser et que vous devez vous connecter à un service Web utilisant le style RPC/codé, vous pouvez utiliser un service de proxy .NET pour vous y connecter.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-110">However, if you do not control the Web service that you want to work with, and you must connect to a Web service uses the RPC/encoded style, you can use a .NET proxy service to connect to an RPC/encoded Web service.</span></span>
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a><span data-ttu-id="2dd8a-111">Utilisation d'un service de proxy .NET pour se connecter à un service Web</span><span class="sxs-lookup"><span data-stu-id="2dd8a-111">Using a .NET Proxy Service to Connect to a Web Service</span></span>

<span data-ttu-id="2dd8a-p103">Si vous ne contrôlez pas le service Web RPC/codé que vous voulez utiliser, vous pouvez créer un service Web de proxy Microsoft .NET de type document/littéral qui fournit des fonctions de wrapper pour chacune des méthodes Web que vous voulez appeler depuis le service Web RPC/codé. Vous pouvez ensuite utiliser le service Web de proxy document/littéral depuis InfoPath.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-p103">If you do not control the RPC/encoded Web service that you want to work with, you can create a document/literal proxy Microsoft .NET Web service that provides wrapper functions for each of the Web methods, you want to invoke from the RPC/encoded Web service. You can then work with the proxy document/literal Web service from InfoPath.</span></span>
  
<span data-ttu-id="2dd8a-p104">Le code .NET Framework peut fonctionner avec tous les types de services Web (RPC/codé et document/littéral), et tous les services Web .NET utilisent le style et le codage document/littéral. .NET Framework pouvant communiquer avec tous les types de services Web, vous pouvez créer un service Web .NET qui a des méthodes effectuant des appels au service Web RPC/codé. Le service Web .NET agira en tant que traducteur, permettant à InfoPath d'effectuer des appels de style document/littéral au service Web .NET, qui à son tour peut effectuer des appels de style RPC/codé au service Web d'origine.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-p104">.NET Framework code can work with any kind of Web service (both RPC/encoded and document/literal), and all .NET Web services use the document/literal style and encoding. Because the .NET Framework can communicate with any kind of Web service, you can create a .NET Web service that has methods that make calls to the RPC/encoded Web service. The .NET Web service will act as a translator that enables InfoPath to make document/literal style calls to the .NET Web service which in turn can make RPC/encoded style calls to the original Web service.</span></span>
  
<span data-ttu-id="2dd8a-p105">Les préalables à la création d'un tel service de proxy Microsoft .NET Web sont un ordinateur Microsoft Windows ou Microsoft Windows Server exécutant les services Internet (IIS) avec ASP.NET installé, sur lequel le service Web de proxy peut être déployé. Lorsque vous créez une solution InfoPath, vous pointez vers le service Web de proxy au lieu du service Web RPC/codé. Le service Web de proxy effectue alors des appels au service RPC/codé.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-p105">The prerequisites for creating such a proxy Microsoft .NET Web service are a Microsoft Windows or Microsoft Windows Server computer that is running Internet Information Services (IIS) with ASP.NET installed on which to deploy the proxy Web service. When you create an InfoPath solution, you will point to the proxy Web service instead of the RPC/encoded Web service. The proxy Web service will then make calls to the RPC/encoded service.</span></span>
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a><span data-ttu-id="2dd8a-120">Création d'un service Web de proxy à l'aide de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2dd8a-120">Creating a Proxy Web Service Using Visual Studio</span></span>

1. <span data-ttu-id="2dd8a-121">Créez un nouveau projet **Application de service Web ASP.NET**.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-121">Create a new **ASP.NET Web Service Application** project.</span></span> 
    
2. <span data-ttu-id="2dd8a-122">Dans l' **Explorateur de solutions**, cliquez avec le bouton droit sur le dossier **Références** de votre nouveau projet, puis cliquez sur **Ajouter une référence Web**.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-122">In the **Solution Explorer**, right-click the **References** folder of your new project, and then click **Add Web Reference**.</span></span> 
    
3. <span data-ttu-id="2dd8a-123">Dans la boîte de dialogue **Ajouter une référence Web**, entrez l'URL du service Web RPC/codé que vous voulez utiliser, puis cliquez sur **Aller à**.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-123">In the **Add Web Reference** dialog box, type in the URL of the RPC/encoded Web service that you want to work with, and then click **Go**.</span></span>
    
4. <span data-ttu-id="2dd8a-124">Cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-124">Click **Add Reference**.</span></span> 
    
5. <span data-ttu-id="2dd8a-125">Ouvrez le fichier .asmx pour votre service Web et ajoutez une méthode de service Web pour appeler chaque méthode de service Web depuis le service Web RPC/codé référencé.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-125">Open the .asmx file for your Web service and add one Web Service method to call each Web Service method from the referenced RPC/encoded Web service.</span></span>
    
6. <span data-ttu-id="2dd8a-p106">Pour afficher une liste des méthodes dans le serveur Web RPC/codé de référence, affichez la fenêtre **Affichage de classes**. Pour chaque méthode de service Web, vous voyez trois méthodes. Par exemple, si la méthode de service Web est appelée  `doSearch`, vous voyez trois méthodes appelées  `doSearch`,  `BegindoSearch` et  `EnddoSearch`. Vous devez créer un service Web de wrapper seulement pour la méthode  `doSearch`. Vérifiez que vous utilisez exactement la signature et le type de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-p106">To view a list of the methods in the reference RPC/encoded Web server, display the **Class View** window. For each Web Service method, you will see three methods. For example, if the Web Service method is called  `doSearch`, then you will see three methods called  `doSearch`,  `BegindoSearch`, and  `EnddoSearch`. You only have to create a wrapper Web Service method for the  `doSearch` method. Be sure to match the exact method signature and return type.</span></span> 
    
7. <span data-ttu-id="2dd8a-131">Dans chaque méthode de wrapper, vous devez écrire du code pour effectuer un appel au service Web RPC/codé référencé, comme dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-131">Within each wrapper method, you have to write code to make a call to the referenced RPC/encoded Web service as shown in the following example.</span></span> 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. <span data-ttu-id="2dd8a-132">Si le service Web RPC/codé requiert une authentification, vous pouvez coder en dur les informations d'identification requises pour la connexion au service Web RPC/codé dans le code source pour le service Web .NET de proxy ou bien vous pouvez utiliser du code similaire à l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-132">If the RPC/encoded Web service requires authentication, you can hard code the credentials required to connect to the RPC/encoded Web service into the source code for the proxy .NET Web service, or you can use code like the following example.</span></span> 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

<span data-ttu-id="2dd8a-133">Pour plus d'informations, recherchez l'article de la Base de connaissances Microsoft « Procédure : passage des informations d'identification actuelles à un service Web ASP.NET » sur http://support.microsoft.com/.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-133">For more information, search for the Microsoft Knowledge Base article "HOW TO: Pass Current Credentials to an ASP.NET Web Service" on http://support.microsoft.com/.</span></span>
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a><span data-ttu-id="2dd8a-134">Création d'un service Web de proxy sans Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="2dd8a-134">Creating a Proxy Web Service Without Visual Studio .NET</span></span>

<span data-ttu-id="2dd8a-135">Il est également possible de créer un service Web de proxy à l'aide des outils fournis avec le Kit de développement logiciel (SDK) .NET Framework, qui peut être téléchargé sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-135">Alternatively, you can create a proxy Web service by using the tools that are provided with the .NET Framework Software Development Kit, which can be downloaded from MSDN.</span></span>
  
<span data-ttu-id="2dd8a-p107">Utilisez l'outil Web Services Description Language (Wsdl.exe) pour créer le fichier de code pour votre service Web de proxy. Ce fichier de code peut être compilé à l'aide du compilateur en ligne de commande C# (csc.exe) ou du compilateur en ligne de commande Visual Basic .NET (vbc.exe), qui font également partie du SDK .NET Framework. Après que l'outil Web Services Description Language a généré le fichier de code, renommez l'extension du nom de fichier en .asmx et ouvrez le fichier dans un éditeur de texte. Sur la toute première ligne du document, ajoutez la directive de page suivante :</span><span class="sxs-lookup"><span data-stu-id="2dd8a-p107">Use the Web Services Description Language Tool (Wsdl.exe) to create the code file for your proxy Web service. This code file can be compiled by using the C# command-line compiler (csc.exe) or the Visual Basic .NET command-line compiler (vbc.exe), which are also included with the .NET Framework SDK. After the Web Services Description Language tool has generated the code file, rename the file name extension to .asmx and open the file in any text editor. On the very first line of the document, add the following page directive:</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

<span data-ttu-id="2dd8a-p108">Allez à la fin du fichier de code et créez un appel à chacune des méthodes de service Web du service Web RPC/codé. L'exemple de code suivant montre le code pour un service Web .NET qui se connecte au service Web Google, qui utilise le style de développement RPC/codé. Il y a un espace réservé pour le code généré par wsdl.exe.</span><span class="sxs-lookup"><span data-stu-id="2dd8a-p108">Go to the end of the code file and create a call to each Web Service method in the RPC/encoded Web service. The following code sample shows the code for a .NET Web service that connects to the Google Web service, which uses the RPC/encoded style of development. There is a placeholder for where the wsdl.exe generated code should go.</span></span>
  
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


