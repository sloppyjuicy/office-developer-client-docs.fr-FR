---
title: Obtenir des informations sur les magasins dans un profil
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0229294cd6655f9017780ee0d9a7a23de76f2362
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406567"
---
# <a name="get-information-about-stores-in-a-profile"></a>Obtenir des informations sur les magasins dans un profil

Cet exemple montre comment obtenir et énumérer les magasins dans un profil.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Vous pouvez utiliser la collection [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) pour énumérer les magasins pour un profil donné. La collection **Stores** fournit des membres qui exposent des informations sur chaque objet [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) , telles que le moment où un objet **Store** a été ajouté ou le moment où un objet **Store** va être supprimé du profil actif. Dans l’exemple de code suivant, EnumerateStores obtient l’objet **Stores** qui représente les magasins du profil actif, et énumère les magasins. L'objet EnumerateStores examine chaque objet **Store** de la collection **Stores**. Si la propriété [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) retourne **true**, indiquant qu'il existe une banque avec une extension .pst ou .ost, les propriétés [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) et [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) sont écrites sur les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateStores()
{
    Outlook.Stores stores = Application.Session.Stores;
    foreach (Outlook.Store store in stores)
    {
        if (store.IsDataFileStore == true)
        {
            Debug.WriteLine(String.Format("Store: "
            + store.DisplayName
            + "\n" + "File Path: "
            + store.FilePath + "\n"));
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Magasins](stores.md)

