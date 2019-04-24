---
title: Affichage des listes d’adresses d’un profil
TOCTitle: Display the address lists for a profile
ms:assetid: ced8230b-110b-4ccb-a699-588798144154
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184643(v=office.15)
ms:contentKeyID: 55119802
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b69ed930241dc058b22b75c6ccc9121f8856d28f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356370"
---
# <a name="display-the-address-lists-for-a-profile"></a>Affichage des listes d’adresses d’un profil

Cet exemple montre comment afficher les listes d’adresses du profil actuel.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Le profil actif contient des listes d'adresses représentées par la collection [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)) . Pour obtenir une instance de la collection AddressLists, vous devez utiliser la propriété [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) .

Dans l’exemple de code suivant, EnumerateAddressLists commence par énumérer chaque objet [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) de la collection AddressLists à l’aide d’une instruction foreach. Une chaîne contenant les valeurs des propriétés [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)) et [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)) est ensuite créée. Enfin, EnumerateAddressLists écrit la chaîne dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx). Cela permet d’afficher les listes d’adresses du profil actuel.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAddressLists()
{
    Outlook.AddressLists addrLists =
         Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Display Name: " + addrList.Name);
        sb.AppendLine("Resolution Order: "
            + addrList.ResolutionOrder.ToString());
        sb.AppendLine("Read-only : "
            + addrList.IsReadOnly.ToString());
        sb.AppendLine("Initial Address List: "
            + addrList.IsInitialAddressList.ToString());
        sb.AppendLine("");
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Carnet d’adresses](address-book.md)

