---
title: Obtention des informations de toutes les listes de distribution dont l’utilisateur actuel est membre
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bbc87250ab77f662e0fc5a71f9857e734637dd2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702753"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a>Obtention des informations de toutes les listes de distribution dont l’utilisateur actuel est membre

Cet exemple utilise la méthode [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) pour obtenir des informations sur toutes les listes de distribution dont l’utilisateur actuel est membre.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans l’exemple de code suivant, GetCurrentUserMembership appelle la méthode **GetMemberOfList** afin d’obtenir une collection [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) pour toutes les listes de distribution dont l’utilisateur Exchange est membre. Si l’utilisateur n’est pas membre d’une liste de distribution, **GetMemberOfList** renvoie une collection **AddressEntries** qui a un décompte de zéro. L’utilisateur doit être en ligne pour que **GetMemberOfList** renvoie une collection **AddressEntries**. Sinon, **GetMemberOfList** renvoie une référence Null. GetCurrentUserMembership utilise la méthode [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)), qui renvoie l’objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) actuel pour tester si l’utilisateur est en ligne. Une fois les entrées d’adresse obtenues, l’exemple écrit des informations sur chacune des listes de distribution de l’utilisateur dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Utilisateurs Exchange](exchange-users.md)

