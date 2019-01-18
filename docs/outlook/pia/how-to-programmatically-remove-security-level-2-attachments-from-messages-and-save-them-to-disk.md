---
title: Supprimer par programmation des pièces jointes de niveau 2 de sécurité des messages et les enregistrer sur disque
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 135f07f4bd3bdc36cee8547106b955b967150df8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706932"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a>Supprimer par programmation des pièces jointes de niveau 2 de sécurité des messages et les enregistrer sur disque

Cet exemple montre comment supprimer les pièces jointes de niveau de sécurité 2 des messages électroniques et comment les enregistrer sur disque d’où elles peuvent être ouvertes.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Outlook protège les utilisateurs contre le code malveillant véhiculé via des pièces jointes de courrier électronique portant une extension particulière, comme .exe ou .bat. Ces pièces jointes spécifiques sont bloquées par défaut et identifiées en tant que pièces jointes de niveau 1. Les pièces jointes de niveau 2 présentent moins de risque de contenir du code malveillant, mais les utilisateurs ne peuvent pas les ouvrir directement à partir du message électronique. Une pièce jointe de niveau 2 doit tout d’abord être enregistrée sur un disque.

À l’aide de la méthode [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) dans l’objet [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)), vous pouvez enregistrer des pièces jointes sur un disque. Dans l’exemple de code suivant, RemoveAttachmentsAndSaveToDisk commence par supprimer toutes les pièces jointes de niveau 2 dans les éléments de courrier d’un dossier spécifique dont la taille est supérieure à celle spécifiée. Pour cela, la propriété [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) de chaque objet **Attachment** de la collection [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) est énumérée et les propriétés ayant la valeur [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)) sont supprimées. RemoveAttachmentsAndSaveToDisk enregistre ensuite la pièce jointe supprimée à l’aide de la méthode **SaveAsFile**.

> [!NOTE] 
> Dans Outlook, les collections sont linéaires. Utilisez l’opérateur [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) pour référencer **Attachments**[1] à **Attachments**[n], où n représente la valeur de la propriété [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia).
> 
> Vous ne pouvez pas utiliser une instruction **foreach** pour supprimer les éléments d’une collection. Utilisez à la place un opérateur **Index** pour obtenir le premier élément de la collection, puis supprimez cet élément. Utilisez ensuite une instruction **while** pour déterminer à quel moment vous avez supprimé le nombre approprié d’éléments dans la collection. Vous serez ainsi assuré d’avoir itéré sur le nombre correct d’éléments dans la collection.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Pièces jointes](attachments.md)

