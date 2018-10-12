---
title: Supprimer par programmation des pièces jointes de niveau 2 de sécurité des messages et les enregistrer sur disque
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 3646ff17a6200a6b46b7796537a40e7bdab40781
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406595"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a><span data-ttu-id="2ba43-102">Supprimer par programmation des pièces jointes de niveau 2 de sécurité des messages et les enregistrer sur disque</span><span class="sxs-lookup"><span data-stu-id="2ba43-102">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>

<span data-ttu-id="2ba43-103">Cet exemple montre comment supprimer les pièces jointes de niveau de sécurité 2 des messages électroniques et comment les enregistrer sur disque d’où elles peuvent être ouvertes.</span><span class="sxs-lookup"><span data-stu-id="2ba43-103">This example shows how to remove security Level 2 attachments from e-mail messages and save them to a disk, from where they can be opened.</span></span>

## <a name="example"></a><span data-ttu-id="2ba43-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="2ba43-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2ba43-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="2ba43-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="2ba43-106">Outlook protège les utilisateurs contre le code malveillant véhiculé via des pièces jointes de courrier électronique portant une extension particulière, comme .exe ou .bat.</span><span class="sxs-lookup"><span data-stu-id="2ba43-106">Outlook protects users from malicious code transported via e-mail attachments that have certain file extensions such as .exe or .bat.</span></span> <span data-ttu-id="2ba43-107">Ces pièces jointes spécifiques sont bloquées par défaut et identifiées en tant que pièces jointes de niveau 1.</span><span class="sxs-lookup"><span data-stu-id="2ba43-107">Those particular attachments are blocked by default and identified as Level 1 attachments.</span></span> <span data-ttu-id="2ba43-108">Les pièces jointes de niveau 2 présentent moins de risque de contenir du code malveillant, mais les utilisateurs ne peuvent pas les ouvrir directement à partir du message électronique.</span><span class="sxs-lookup"><span data-stu-id="2ba43-108">Level 2 attachments have a lesser chance of containing malicious code, but users cannot open a Level 2 attachment directly from an e-mail message.</span></span> <span data-ttu-id="2ba43-109">Une pièce jointe de niveau 2 doit tout d’abord être enregistrée sur un disque.</span><span class="sxs-lookup"><span data-stu-id="2ba43-109">A Level 2 attachment must first be saved to a disk.</span></span>

<span data-ttu-id="2ba43-110">À l’aide de la méthode [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) dans l’objet [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)), vous pouvez enregistrer des pièces jointes sur un disque.</span><span class="sxs-lookup"><span data-stu-id="2ba43-110">By using the [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) method in the [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) object, you can save attachments to a disk.</span></span> <span data-ttu-id="2ba43-111">Dans l’exemple de code suivant, RemoveAttachmentsAndSaveToDisk commence par supprimer toutes les pièces jointes de niveau 2 dans les éléments de courrier d’un dossier spécifique dont la taille est supérieure à celle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2ba43-111">In the following code example,   first removes from mail items in a folder all Level 2 attachments that are greater than a specified size.</span></span> <span data-ttu-id="2ba43-112">Pour cela, la propriété [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) de chaque objet **Attachment** de la collection [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) est énumérée et les propriétés ayant la valeur [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)) sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="2ba43-112">This is done by enumerating the [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) property of each **Attachment** object in the [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) collection and removing the ones that are equal to [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)) .</span></span> <span data-ttu-id="2ba43-113">RemoveAttachmentsAndSaveToDisk enregistre ensuite la pièce jointe supprimée à l’aide de la méthode **SaveAsFile**.</span><span class="sxs-lookup"><span data-stu-id="2ba43-113"> then saves the removed attachment by using the SaveAsFile method.</span></span>

> [!NOTE] 
> <span data-ttu-id="2ba43-114">Dans Outlook, les collections sont linéaires.</span><span class="sxs-lookup"><span data-stu-id="2ba43-114">[!C# NOTE] Collections in Outlook are linear.</span></span> <span data-ttu-id="2ba43-115">Utilisez l’opérateur [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) pour référencer **Attachments**[1] à **Attachments**[n], où n représente la valeur de la propriété [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="2ba43-115">Use the Index [n] operator to reference Attachments[1] to Attachments[ ] where   represents the value of the Count property.</span></span>
> 
> <span data-ttu-id="2ba43-p104">Vous ne pouvez pas utiliser une instruction **foreach** pour supprimer les éléments d’une collection. Utilisez à la place un opérateur **Index** pour obtenir le premier élément de la collection, puis supprimez cet élément. Utilisez ensuite une instruction **while** pour déterminer à quel moment vous avez supprimé le nombre approprié d’éléments dans la collection. Vous serez ainsi assuré d’avoir itéré sur le nombre correct d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2ba43-p104">You cannot use a **foreach** statement to remove items in a collection. Instead, use an **Index** operator to obtain the first item in the collection, and then delete the item. Then use a **while** statement to determine when you have deleted the appropriate number of items in the collection. This will ensure that you have iterated over the correct number of items in the collection.</span></span>

<span data-ttu-id="2ba43-120">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="2ba43-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="2ba43-121">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="2ba43-121">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="2ba43-122">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="2ba43-122">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RemoveAttachmentsAndSaveToDisk(string path,
    Outlook.Folder folder, int size)
{
    Outlook.Items attachItems;
    Outlook.Attachment attachment;
    Outlook.Attachments attachments;
    int byValueCount;
    int removeCount;
    bool saveMessage;
    try
    {
        // The restriction will find all items that
        // have attachments and MessageClass = IPM.Note.
        string filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:hasattachment"
            + "\"" + " = True" + " AND " + "\""
            + "https://schemas.microsoft.com/mapi/proptag/0x001A001E"
            + "\"" + " = 'IPM.Note'";
        attachItems = folder.Items.Restrict(filter);
        foreach (Outlook.MailItem mail in attachItems)
        {
            saveMessage = false;
            byValueCount = 0;
            attachments = mail.Attachments;
            // Obtain the count of ByValue attachments.
            foreach (Outlook.Attachment attach in attachments)
            {
                if (attach.Size > size
                    & attach.Type ==
                    Outlook.OlAttachmentType.olByValue)
                {
                    byValueCount = byValueCount + 1;
                }
            }
            if (byValueCount > 0)
            {
                // removeCount is number of attachments to remove.
                removeCount = attachments.Count - byValueCount;
                while (mail.Attachments.Count != removeCount)
                {
                    // Use indexer to obtain 
                    // first attachment in collection.
                    attachment = mail.Attachments[1];
                    // You can refine this code to save 
                    // separate copies of attachments 
                    // with the same name.
                    attachment.SaveAsFile(path + @"\"
                        + attachment.FileName);
                    attachment.Delete();
                    if (saveMessage != true)
                    {
                        saveMessage = true;
                    }
                }
                if (saveMessage)
                {
                    mail.Save();
                }
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="2ba43-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ba43-123">See also</span></span>

- [<span data-ttu-id="2ba43-124">Pièces jointes</span><span class="sxs-lookup"><span data-stu-id="2ba43-124">Attachments</span></span>](attachments.md)

