---
title: Obtention du compte lié à un dossier
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d83a145b577cbc9be68cdd694f7806da7cdad512
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407204"
---
# <a name="get-the-account-for-a-folder"></a><span data-ttu-id="a93d0-102">Obtention du compte lié à un dossier</span><span class="sxs-lookup"><span data-stu-id="a93d0-102">Get the account for a folder</span></span>

<span data-ttu-id="a93d0-103">Cet exemple obtient le compte associé à un dossier dans la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="a93d0-103">This example gets the account that is associated with a folder in the current session.</span></span>

## <a name="example"></a><span data-ttu-id="a93d0-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="a93d0-104">Example</span></span>

<span data-ttu-id="a93d0-105">Dans l’exemple de code suivant, la fonction DisplayAccountForCurrentFolder appelle la fonction GetAccountForFolder pour identifier le compte dont la banque de remise par défaut héberge le dossier actif, puis affiche le nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="a93d0-105">In the following code example, the   function calls the   function to identify the account whose default delivery store hosts the current folder, and then displays the name of the folder.</span></span> <span data-ttu-id="a93d0-106">GetAccountForFolder met en correspondance la banque du dossier actif (obtenue à partir de la propriété [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) et la banque de remise par défaut de chaque compte (obtenue à partir de la propriété [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) qui est définie dans la collection [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) de la session.</span><span class="sxs-lookup"><span data-stu-id="a93d0-106"> matches the store of the current folder (obtained from the Store property) with the default delivery store of each account (obtained with the DeliveryStore property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="a93d0-107">La fonction GetAccountForFolder renvoie l’objet [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) si une correspondance est trouvée. Sinon, elle renvoie une référence Null.</span><span class="sxs-lookup"><span data-stu-id="a93d0-107"> returns the Account object if a match is found; otherwise, it returns a null reference.</span></span>

<span data-ttu-id="a93d0-p102">Dans une session Microsoft Outlook dans le profil de laquelle plusieurs comptes sont définis, le dossier affiché dans l'explorateur actif ne réside pas nécessairement dans la banque par défaut de cette session ; au lieu de cela, il peut résider dans l'une des multiples banques associées aux différents comptes. Cette rubrique montre comment identifier le compte dont la banque de remise par défaut est celle qui héberge le dossier.</span><span class="sxs-lookup"><span data-stu-id="a93d0-p102">In a Microsoft Outlook session that has multiple accounts defined in the profile, the folder that is displayed in the active explorer does not necessarily reside on the default store for that session; instead, it can reside on one of the multiple stores associated with the multiple accounts. This topic shows how to identify the account whose default delivery store is the same store that hosts the folder.</span></span>

<span data-ttu-id="a93d0-110">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a93d0-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="a93d0-111">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="a93d0-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="a93d0-112">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="a93d0-112">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a93d0-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a93d0-113">See also</span></span>

- [<span data-ttu-id="a93d0-114">Comptes</span><span class="sxs-lookup"><span data-stu-id="a93d0-114">Accounts</span></span>](accounts.md)

