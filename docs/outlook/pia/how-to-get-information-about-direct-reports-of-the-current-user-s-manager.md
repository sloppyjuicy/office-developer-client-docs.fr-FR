---
title: Obtention des informations des collaborateurs directs du responsable de l’utilisateur actuel
TOCTitle: Get information about direct reports of the current user's manager
ms:assetid: 768bf573-1b10-4776-8947-a7f8dc3ebde0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184617(v=office.15)
ms:contentKeyID: 55119842
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6237b3455eea449460133fb52a79ef87bcaebc1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406700"
---
# <a name="get-information-about-direct-reports-of-the-current-users-manager"></a>Obtention des informations des collaborateurs directs du responsable de l’utilisateur actuel

Cet exemple obtient les subordonnés du responsable de l’utilisateur actif, le cas échéant, puis affiche des informations sur chaque subordonné du responsable.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans l’exemple suivant, la procédure GetManagerDirectReports appelle la méthode [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) pour obtenir le responsable de l’utilisateur, représenté par un objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)). Si l’utilisateur actif a un responsable, la méthode [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) est appelée pour renvoyer une collection [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) qui représente les entrées d’adresse de tous les collaborateurs directs du responsable de l’utilisateur. Si le responsable n’a aucun collaborateur direct, **GetDirectReports** renvoie une collection **AddressEntries** qui a un décompte de zéro. Une fois les collaborateurs directs du responsable obtenus, GetManagerDirectReports écrit des informations sur chacun des collaborateurs directs du responsable dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).


> [!NOTE]
> L’utilisateur doit être en ligne pour que cette méthode renvoie une collection **AddressEntries**. Sinon, **GetDirectReports** renvoie une référence Null. Pour le code de production, vous devez tester que l’utilisateur est hors connexion à l’aide de la propriété [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) ou [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) pour plusieurs scénarios Exchange.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerDirectReports()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.AddressEntries addrEntries =
                manager.GetDirectReports();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Outlook.ExchangeUser exchUser =
                        addrEntry.GetExchangeUser();
                    StringBuilder sb = new StringBuilder();
                    sb.AppendLine("Name: "
                        + exchUser.Name);
                    sb.AppendLine("Title: "
                        + exchUser.JobTitle);
                    sb.AppendLine("Department: "
                        + exchUser.Department);
                    sb.AppendLine("Location: "
                        + exchUser.OfficeLocation);
                    Debug.WriteLine(sb.ToString());
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Utilisateurs Exchange](exchange-users.md)

