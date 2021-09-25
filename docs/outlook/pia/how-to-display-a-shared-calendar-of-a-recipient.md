---
title: Afficher un calendrier partagé d’un destinataire
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5775c7856ecf5d4e163f5c27e9aeca3ab55920bb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560605"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a>Afficher un calendrier partagé d’un destinataire

Cet exemple montre comment afficher le calendrier partagé d’un destinataire à l’aide des méthodes [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) et [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Les éléments qui peuvent être expédiés, tels que les objets [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) , exposent toujours la propriété [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) qui, à son tour, vous permet d'accéder à la collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) de l'élément expédiable. Pour créer un objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) qui n'est pas lié à la collection **Recipients** d'un élément, utilisez la méthode [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . Passez ensuite cet objet **Recipient** non lié à la méthode [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) , qui retourne un dossier Exchange partagé. Vous pouvez alors ouvrir le dossier Exchange partagé et l'afficher dans une fenêtre d'explorateur. La méthode GetSharedDefaultFolder s'utilise dans les scénarios de délégation Exchange dans lesquels le délégué est autorisé à accéder au dossier du délégateur. Avant de passer l'objet **Recipient** à la méthode GetSharedDefaultFolder, vous devez le résoudre. Pour résoudre un objet **Recipient**, appelez sa méthode [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) .

Dans l’exemple de code suivant, DisplayManagerCalendar ouvre et afficher le dossier Calendrier du Responsable de l’utilisateur actif en appelant **CreateRecipient** et **GetSharedDefaultFolder**. Une boîte de dialogue d’alerte s’affiche si l’utilisateur n’est pas autorisé à ouvrir le dossier Calendrier du Responsable ou si une erreur se produit. 


> [!NOTE]
> Lorsque vous créez un objet **Recipient** à l'aide de la méthode **CreateRecipient** de l'objet **Namespace** ou de la méthode [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) de la collection **Recipients**, vous devez spécifier un nom de destinataire. L’objet **Recipient** est ensuite résolu par rapport à ce nom. Le nom d’un destinataire peut être dans l’un des formats suivants :
> - Nom
> - Alias
> - Adresse SMTP (Simple Mail Transfer Protocol)

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayManagerCalendar()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.Recipient recip =
                Application.Session.CreateRecipient(manager.Name);
            if (recip.Resolve())
            {
                try
                {
                    Outlook.Folder folder =
                        Application.Session.GetSharedDefaultFolder(
                        recip, Outlook.OlDefaultFolders.olFolderCalendar)
                        as Outlook.Folder;
                    folder.Display();
                }
                catch
                {
                    MessageBox.Show("Could not open manager's calendar.",
                        "GetSharedDefaultFolder Example",
                        MessageBoxButtons.OK,
                        MessageBoxIcon.Error);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Calendar](calendar.md)

