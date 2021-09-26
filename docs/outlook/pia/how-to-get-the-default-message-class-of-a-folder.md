---
title: Obtention de la classe de message par défaut d’un dossier
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 78646e5ef2263d7478eb3caf54c83d41e4eff890
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583141"
---
# <a name="get-the-default-message-class-of-a-folder"></a>Obtention de la classe de message par défaut d’un dossier

Cet exemple montre comment utiliser la propriété [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) pour obtenir la classe de message par défaut d’un dossier.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Pour obtenir la classe de message par défaut d’un dossier, utilisez la propriété **DefaultMessageClass** de l’objet [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)). Par exemple, un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) avec IPM.Contact comme **DefaultMessageClass** représente un dossier Contact. Cependant, si le formulaire par défaut du dossier est un formulaire personnalisé ou un formulaire de remplacement, vous devez utiliser l'objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) pour déterminer la classe de message du formulaire par défaut. La propriété **DefaultMessageClass** ne renvoie pas la classe de message du formulaire par défaut du dossier.

Dans l’exemple de code suivant, la procédure GetDefaultMessageClass utilise **PropertyAccessor** pour déterminer le formulaire par défaut d’un dossier. Si la propriété de dossier **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) est introuvable et qu’Outlook déclenche une erreur, le bloc **try…catch** renvoie la propriété **DefaultMessageClass** de **Folder**.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"http://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Dossiers](folders.md)

