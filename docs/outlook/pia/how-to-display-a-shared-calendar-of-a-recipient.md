---
title: Afficher un calendrier partagé d’un destinataire
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 10101a3eff1b0507c1fe562f175bace7026143fb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406882"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a><span data-ttu-id="631c9-102">Afficher un calendrier partagé d’un destinataire</span><span class="sxs-lookup"><span data-stu-id="631c9-102">Display a shared calendar of a recipient</span></span>

<span data-ttu-id="631c9-103">Cet exemple montre comment afficher le calendrier partagé d’un destinataire à l’aide des méthodes [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) et [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="631c9-103">This example shows how to display a recipient's shared calendar by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) and [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) methods.</span></span>

## <a name="example"></a><span data-ttu-id="631c9-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="631c9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="631c9-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="631c9-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="631c9-p101">Les éléments qui peuvent être expédiés, tels que les objets [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) , exposent toujours la propriété [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) qui, à son tour, vous permet d'accéder à la collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) de l'élément expédiable. Pour créer un objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) qui n'est pas lié à la collection **Recipients** d'un élément, utilisez la méthode [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . Passez ensuite cet objet **Recipient** non lié à la méthode [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) , qui retourne un dossier Exchange partagé. Vous pouvez alors ouvrir le dossier Exchange partagé et l'afficher dans une fenêtre d'explorateur. La méthode GetSharedDefaultFolder s'utilise dans les scénarios de délégation Exchange dans lesquels le délégué est autorisé à accéder au dossier du délégateur. Avant de passer l'objet **Recipient** à la méthode GetSharedDefaultFolder, vous devez le résoudre. Pour résoudre un objet **Recipient**, appelez sa méthode [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="631c9-p101">Sendable items such as [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects always expose the [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) property which, in turn, enables you to access the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection for the sendable item. To create a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object that is not bound to the **Recipients** collection of an item, use the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object. Then pass this unbound **Recipient** object to the [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) method, which returns a shared Exchange folder. You can then open the shared Exchange folder and display that folder in an explorer window. GetSharedDefaultFolder is used in Exchange delegate scenarios where the delegate has permission to access the folder of the delegator. Before you pass the **Recipient** object to the GetSharedDefaultFolder method, you must resolve it. To resolve a **Recipient** object, call its [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) method.</span></span>

<span data-ttu-id="631c9-p102">Dans l’exemple de code suivant, DisplayManagerCalendar ouvre et afficher le dossier Calendrier du Responsable de l’utilisateur actif en appelant **CreateRecipient** et **GetSharedDefaultFolder**. Une boîte de dialogue d’alerte s’affiche si l’utilisateur n’est pas autorisé à ouvrir le dossier Calendrier du Responsable ou si une erreur se produit. </span><span class="sxs-lookup"><span data-stu-id="631c9-p102">In the following code example, DisplayManagerCalendar opens and displays the Calendar folder of the current user’s manager by calling **CreateRecipient** and **GetSharedDefaultFolder**. An alert dialog box is displayed if the user does not have permission to open the manager’s Calendar folder or an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="631c9-115">Lorsque vous créez un objet **Recipient** à l'aide de la méthode **CreateRecipient** de l'objet **Namespace** ou de la méthode [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) de la collection **Recipients**, vous devez spécifier un nom de destinataire.</span><span class="sxs-lookup"><span data-stu-id="631c9-115">When you create a **Recipient** object by using the **CreateRecipient** method of the **Namespace** object or the [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) method of the **Recipients** collection, you must provide a recipient name.</span></span> <span data-ttu-id="631c9-116">L’objet **Recipient** est ensuite résolu par rapport à ce nom.</span><span class="sxs-lookup"><span data-stu-id="631c9-116">The **Recipient** is then resolved against this name.</span></span> <span data-ttu-id="631c9-117">Le nom d’un destinataire peut être dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="631c9-117">A recipient name can take any of the following formats: >  Display name >  Alias >  Simple Mail Transfer Protocol (SMTP) address</span></span>
> - <span data-ttu-id="631c9-118">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="631c9-118">Display name</span></span>
> - <span data-ttu-id="631c9-119">Alias</span><span class="sxs-lookup"><span data-stu-id="631c9-119">Alias</span></span>
> - <span data-ttu-id="631c9-120">Adresse SMTP (Simple Mail Transfer Protocol)</span><span class="sxs-lookup"><span data-stu-id="631c9-120">Simple Mail Transfer Protocol (SMTP) address</span></span>

<span data-ttu-id="631c9-121">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="631c9-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="631c9-122">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="631c9-122">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="631c9-123">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="631c9-123">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="631c9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="631c9-124">See also</span></span>

- [<span data-ttu-id="631c9-125">Calendrier</span><span class="sxs-lookup"><span data-stu-id="631c9-125">Calendar</span></span>](calendar.md)

