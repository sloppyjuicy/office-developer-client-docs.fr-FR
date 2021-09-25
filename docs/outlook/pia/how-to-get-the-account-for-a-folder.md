---
title: Obtention du compte lié à un dossier
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b681e8cdac2f915dcf2e5c74419fb7f4ac6c6752
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590635"
---
# <a name="get-the-account-for-a-folder"></a>Obtention du compte lié à un dossier

Cet exemple obtient le compte associé à un dossier dans la session actuelle.

## <a name="example"></a>Exemple

Dans l’exemple de code suivant, la fonction DisplayAccountForCurrentFolder appelle la fonction GetAccountForFolder pour identifier le compte dont la banque de remise par défaut héberge le dossier actif, puis affiche le nom du dossier. GetAccountForFolder met en correspondance la banque du dossier actif (obtenue à partir de la propriété [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) et la banque de remise par défaut de chaque compte (obtenue à partir de la propriété [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) qui est définie dans la collection [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) de la session. La fonction GetAccountForFolder renvoie l’objet [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) si une correspondance est trouvée. Sinon, elle renvoie une référence Null.

Dans une session Microsoft Outlook dans le profil de laquelle plusieurs comptes sont définis, le dossier affiché dans l'explorateur actif ne réside pas nécessairement dans la banque par défaut de cette session ; au lieu de cela, il peut résider dans l'une des multiples banques associées aux différents comptes. Cette rubrique montre comment identifier le compte dont la banque de remise par défaut est celle qui héberge le dossier.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayAccountForCurrentFolder()
{
    Outlook.Folder myFolder = Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    string msg = "Account for Current Folder:" + "\n" +
        GetAccountForFolder(myFolder).DisplayName;
    MessageBox.Show(msg,
        "GetAccountForFolder",
        MessageBoxButtons.OK,
        MessageBoxIcon.Information);
}

Outlook.Account GetAccountForFolder(Outlook.Folder folder)
{
    // Obtain the store on which the folder resides.
    Outlook.Store store = folder.Store;

    // Enumerate the accounts defined for the session.
    foreach (Outlook.Account account in Application.Session.Accounts)
    {
        // Match the DefaultStore.StoreID of the account
        // with the Store.StoreID for the currect folder.
        if (account.DeliveryStore.StoreID  == store.StoreID)
        {
            // Return the account whose default delivery store
            // matches the store of the given folder.
            return account;
        }
     }
     // No account matches, so return null.
     return null;
}
```

## <a name="see-also"></a>Voir aussi

- [Comptes](accounts.md)

