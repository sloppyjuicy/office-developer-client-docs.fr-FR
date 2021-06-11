---
title: Abonnement à un flux RSS
TOCTitle: Subscribe to an RSS feed
ms:assetid: 7ecefbcd-1a34-48e8-afac-7d54e79fd159
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424473(v=office.15)
ms:contentKeyID: 55119852
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b92c733c5030ce12eb691bba57afb5ce6b9d1dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335398"
---
# <a name="subscribe-to-an-rss-feed"></a><span data-ttu-id="d4f76-102">Abonnement à un flux RSS</span><span class="sxs-lookup"><span data-stu-id="d4f76-102">Subscribe to an RSS feed</span></span>

<span data-ttu-id="d4f76-103">Cet exemple montre comment s’abonner à un flux RSS à l’aide de la méthode [OpenSharedFolder (String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d4f76-103">This example shows how to subscribe to an RSS feed by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="d4f76-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="d4f76-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d4f76-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="d4f76-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="d4f76-p101">Le modèle objet Outlook prend en charge la fourniture d'accès à des données partagées, comme des calendriers Internet, des flux RSS et des données de listes ou de bibliothèques de documents Microsoft SharePoint. Il permet de se connecter à ces sources partagées de données et de configurer des contextes de synchronisation pour continuer à interroger ces ressources partagées. Le modèle objet Outlook fournit la méthode [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) pour télécharger et synchroniser avec un type particulier de dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="d4f76-p101">The Outlook object model supports providing access to shared data, such as Internet calendars, RSS feeds, and data from Microsoft SharePoint lists and document libraries. It enables connecting to these shared sources of data and setting up the synchronization contexts to continue to poll those shared resources. The Outlook object model provides the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to download and synchronize with a particular type of shared folder.</span></span>

<span data-ttu-id="d4f76-p102">Dans l’exemple suivant, AddRssFeed s’abonne à un nouveau flux RSS nommé « Example RSS Feed » en appelant la méthode **OpenSharedFolder** avec une URL qui fait référence à ce flux RSS. Les deux derniers paramètres de la méthode **OpenSharedFolder** sont définis à **true** pour indiquer que les pièces jointes doivent être téléchargées et qu’Outlook doit utiliser le ratio d’actualisation fourni dans le flux RSS.</span><span class="sxs-lookup"><span data-stu-id="d4f76-p102">In the following example, AddRssFeed subscribes to a new RSS feed named “Example RSS Feed” by calling the **OpenSharedFolder** method with a URL that refers to the new RSS feed. The last two parameters of **OpenSharedFolder** method are set to **true** to indicate that attachments should be downloaded, and Outlook should use the refresh ratio provided in the RSS feed.</span></span>


> [!NOTE]
> <span data-ttu-id="d4f76-111">Vous devez spécifier le gestionnaire de protocole correct pour l’URL du dossier dans la méthode **OpenSharedFolder** pour vous abonner à un flux RSS.</span><span class="sxs-lookup"><span data-stu-id="d4f76-111">You must specify the correct protocol handler for the folder URL in the **OpenSharedFolder** method to subscribe to an RSS feed.</span></span> <span data-ttu-id="d4f76-112">Par exemple, vous devez utiliser une URL qui commence par `feed://` au lieu de `https://`.</span><span class="sxs-lookup"><span data-stu-id="d4f76-112">For example, you must use a URL that begins with `feed://` instead of `https://`.</span></span> <span data-ttu-id="d4f76-113">Outlook ne peut pas ouvrir les flux RSS qui requièrent une authentification, sauf si l'authentification NTLM (Windows NT LAN Manager) est disponible, et ne peut pas charger les flux RSS depuis des emplacements SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="d4f76-113">Outlook cannot open RSS feeds that require authentication unless Windows NT LAN Manager (NTLM) authentication is available, and it cannot load RSS feeds from Secure Sockets Layer (SSL) locations.</span></span>

<span data-ttu-id="d4f76-114">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d4f76-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="d4f76-115">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="d4f76-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d4f76-116">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="d4f76-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddRssFeed()
{
    string feedUrl = "feed://example.org/rssfeed.xml";
    Outlook.Folder subscriptionFolder =
        Application.Session.OpenSharedFolder(feedUrl, "Example RSS Feed", true, true) as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(subscriptionFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a><span data-ttu-id="d4f76-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4f76-117">See also</span></span>

- [<span data-ttu-id="d4f76-118">Partage de groupe</span><span class="sxs-lookup"><span data-stu-id="d4f76-118">Group sharing</span></span>](group-sharing.md)

