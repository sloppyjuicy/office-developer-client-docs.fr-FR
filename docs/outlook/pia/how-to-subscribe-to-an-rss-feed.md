---
title: Abonnement à un flux RSS
TOCTitle: Subscribe to an RSS feed
ms:assetid: 7ecefbcd-1a34-48e8-afac-7d54e79fd159
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424473(v=office.15)
ms:contentKeyID: 55119852
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 30370e54e25cad6bc4f138f9d8cc0c8a156b8428
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405825"
---
# <a name="subscribe-to-an-rss-feed"></a>Abonnement à un flux RSS

Cet exemple montre comment s’abonner à un flux RSS à l’aide de la méthode [OpenSharedFolder (String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Le modèle objet Outlook prend en charge la fourniture d'accès à des données partagées, comme des calendriers Internet, des flux RSS et des données de listes ou de bibliothèques de documents Microsoft SharePoint. Il permet de se connecter à ces sources partagées de données et de configurer des contextes de synchronisation pour continuer à interroger ces ressources partagées. Le modèle objet Outlook fournit la méthode [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) pour télécharger et synchroniser avec un type particulier de dossier partagé.

Dans l’exemple suivant, AddRssFeed s’abonne à un nouveau flux RSS nommé « Example RSS Feed » en appelant la méthode **OpenSharedFolder** avec une URL qui fait référence à ce flux RSS. Les deux derniers paramètres de la méthode **OpenSharedFolder** sont définis à **true** pour indiquer que les pièces jointes doivent être téléchargées et qu’Outlook doit utiliser le ratio d’actualisation fourni dans le flux RSS.


> [!NOTE]
> Vous devez spécifier le gestionnaire de protocole correct pour l’URL du dossier dans la méthode **OpenSharedFolder** pour vous abonner à un flux RSS. Par exemple, vous devez utiliser une URL qui commence par `feed://` au lieu de `https://`. Outlook ne peut pas ouvrir les flux RSS qui requièrent une authentification, sauf si l'authentification NTLM (Windows NT LAN Manager) est disponible, et ne peut pas charger les flux RSS depuis des emplacements SSL (Secure Sockets Layer).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Partage de groupe](group-sharing.md)

