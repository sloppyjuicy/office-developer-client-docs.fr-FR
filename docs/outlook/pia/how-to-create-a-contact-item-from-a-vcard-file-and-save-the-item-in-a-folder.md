---
title: Création d’un contact à partir d’un fichier vCard et enregistrement du contact dans un dossier
TOCTitle: Create a Contact item from a vCard file and save the item in a folder
ms:assetid: b207b584-ffcf-4ac5-ab1f-4f91d43000e1
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646856(v=office.15)
ms:contentKeyID: 55119826
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a048d090c946ff5a86fddf4b1ac8c6818e061b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321258"
---
# <a name="create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder"></a><span data-ttu-id="09ec3-102">Création d’un contact à partir d’un fichier vCard et enregistrement du contact dans un dossier</span><span class="sxs-lookup"><span data-stu-id="09ec3-102">Create a Contact item from a vCard file and save the item in a folder</span></span>

<span data-ttu-id="09ec3-103">Cet exemple importe tous les fichiers vCard dans un dossier du système de fichiers et enregistre les contacts dans le dossier spécifié par le paramètre *targetFolder*.</span><span class="sxs-lookup"><span data-stu-id="09ec3-103">This example imports all the vCard files in a file system folder and saves the contacts into the folder specified by the *targetFolder* parameter.</span></span>

## <a name="example"></a><span data-ttu-id="09ec3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="09ec3-104">Example</span></span>

<span data-ttu-id="09ec3-p101">Cet exemple utilise la méthode [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)). La méthode **OpenSharedItem** ouvre les messages stockés sous forme de fichiers de message Outlook (.msg), de fichiers de rendez-vous iCalendar (.ics) ou de fichiers vCard (.vcf). Veillez à caster l'objet retourné en type d'élément approprié et appelez la méthode **Save** correspondante pour rendre l'élément persistant. Par défaut, l'élément retourné par la méthode **OpenSharedItem** est enregistré dans le dossier par défaut du type d'élément spécifié. Vous pouvez utiliser la méthode **Move** correspondante pour déplacer un élément dans un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="09ec3-p101">This example uses the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method. The **OpenSharedItem** method opens messages stored as Outlook message format (.msg) files, iCalendar appointment (.ics) files, or vCard (.vcf) files. Be sure to cast the returned object to the appropriate item type and call the corresponding **Save** method to persist the item. By default, the item returned by **OpenSharedItem** is saved in the default folder for the specific item type. You can use the corresponding **Move** method to move the item to a different folder.</span></span>

<span data-ttu-id="09ec3-110">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="09ec3-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="09ec3-111">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="09ec3-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="09ec3-112">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="09ec3-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ImportContacts( _
    ByVal path As String, ByVal targetFolder As Outlook.Folder)
    Dim contact As Outlook.ContactItem
    Dim moveContact As Outlook.ContactItem
    If (Directory.Exists(path)) Then
        Dim files As String() = Directory.GetFiles(path, "*.vcf")
        For Each file As String In files
            contact = CType(Application.Session.OpenSharedItem(file), _
                Outlook.ContactItem)
            If (targetFolder Is _
                CType(Application.Session.GetDefaultFolder( _
                    Outlook.OlDefaultFolders.olFolderContacts) _
                    , Outlook.Folder)) Then
                contact.Save()
            Else
                moveContact = CType(contact.Move(targetFolder), _
                    Outlook.ContactItem)
                moveContact.Save()
            End If
        Next
    End If
End Sub
```


```csharp
private void ImportContacts(string path, Outlook.Folder targetFolder)
{
    Outlook.ContactItem contact;
    Outlook.ContactItem moveContact;
    if (Directory.Exists(path))
    {
        string[] files = Directory.GetFiles(path, "*.vcf");
        foreach (string file in files)
        {
            contact = Application.Session.OpenSharedItem(file)
                as Outlook.ContactItem;
            if (targetFolder ==
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderContacts)
                as Outlook.Folder)
            {
                contact.Save();
            }
            else
            {
                moveContact = contact.Move(targetFolder)
                    as Outlook.ContactItem;
                moveContact.Save();
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="09ec3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09ec3-113">See also</span></span>

- [<span data-ttu-id="09ec3-114">Contacts</span><span class="sxs-lookup"><span data-stu-id="09ec3-114">Contacts</span></span>](contacts.md)

