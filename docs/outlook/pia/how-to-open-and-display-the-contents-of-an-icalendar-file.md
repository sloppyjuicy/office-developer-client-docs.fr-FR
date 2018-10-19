---
title: Ouverture et affichage du contenu d’un fichier iCalendar
TOCTitle: Open and display the contents of an iCalendar file
ms:assetid: 2066e404-7aaf-4fd2-bf5c-9604e3fc2681
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644609(v=office.15)
ms:contentKeyID: 55119818
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dcebc65c651804148969c6260ecac72060bf9ef0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406777"
---
# <a name="open-and-display-the-contents-of-an-icalendar-file"></a><span data-ttu-id="f6077-102">Ouverture et affichage du contenu d’un fichier iCalendar</span><span class="sxs-lookup"><span data-stu-id="f6077-102">Open and display the contents of an iCalendar file</span></span>

<span data-ttu-id="f6077-103">Cet exemple montre comment ouvrir et afficher le contenu d'un fichier iCalendar, selon que le fichier contient un rendez-vous unique ou périodique ou qu'il contient un groupe de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="f6077-103">This example shows how to open and display the contents of an iCalendar file, depending on whether the file contains a single or recurrent appointment, or the file contains a group of appointments.</span></span>

## <a name="example"></a><span data-ttu-id="f6077-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f6077-104">Example</span></span>

<span data-ttu-id="f6077-p101">Cet exemple de code tente d'abord d'utiliser la méthode [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) pour ouvrir le fichier iCalendar en tant que fichier iCalendar de rendez-vous unique. S'il réussit, il affiche les détails de l'élément de rendez-vous dans une fenêtre d'inspecteur. Toutefois, il ne copie pas l'élément dans la banque par défaut. S'il ne parvient pas à ouvrir le fichier en tant que fichier iCalendar de rendez-vous unique, il utilise la méthode [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) de l'objet **NameSpace** pour tenter d'importer le contenu en tant que nouveau calendrier dans la banque par défaut. Si l'importation réussit, il affiche le calendrier dans une fenêtre d'explorateur.</span><span class="sxs-lookup"><span data-stu-id="f6077-p101">This code sample first tries to use the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to open the iCalendar file as a single-appointment iCalendar file. If it succeeds, it will display the appointment item details in an inspector window. However, it will not copy the item to the default store. If the sample cannot open the file as a single-appointment iCalendar file, then it will use the [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the **NameSpace** object to attempt to import the contents as a new calendar in the default store. If it succeeds in importing, then it will display the calendar in an explorer window.</span></span>

<span data-ttu-id="f6077-110">Cet exemple de code permet d’utiliser la classe d’assistance OutlookItem, définie dans la rubrique décrivant comment [créer une classe d’assistance pour permettre d’accéder aux membres éléments Outlook courants](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), pour appeler facilement la méthode **OutlookItem.Display** pour afficher l’élément de rendez-vous sans devoir d’abord distribuer l’élément.</span><span class="sxs-lookup"><span data-stu-id="f6077-110">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the **OutlookItem.Display** method to display the appointment item without having to first cast the item.</span></span>

<span data-ttu-id="f6077-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f6077-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f6077-112">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="f6077-112">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f6077-113">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="f6077-113">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub OpenICalendarFile(ByVal fileName As String)
    If String.IsNullOrEmpty(fileName) Then
        Throw New ArgumentException(_
        "Parameter must contain a value.", "exportFileName")
    End If
    If Not File.Exists(fileName) Then
        Throw New FileNotFoundException(fileName)
    End If

    '' First try to open the icalendar file as an appointment 
    '' (not a calendar folder).
    Dim item As Object = Nothing
    Try
         item = Application.Session.OpenSharedItem(fileName)
    Catch
    End Try

    If Not item Is Nothing Then
        '' Display the item
        Dim olItem As OutlookItem = New OutlookItem(item)
        olItem.Display()
        Return
    End If

    '' If unsucessful in opening it as an item, 
    '' try opening it as a folder
    Dim importedFolder As Outlook.Folder = Nothing
    Try
        importedFolder = TryCast( _
            Application.Session.OpenSharedFolder(fileName), _
            Outlook.Folder)
    Catch
    End Try

    '' If sucessful, open the folder in a new explorer window
    If Not importedFolder Is Nothing Then
        Dim explorer As Outlook.Explorer = _
            Application.Explorers.Add( _
            importedFolder, _
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal)
        explorer.Display()
    End If
End Sub
```


```csharp
private void OpenICalendarFile(string fileName)
{
    if (string.IsNullOrEmpty(fileName))
        throw new ArgumentException("exportFileName", 
        "Parameter must contain a value.");
    if (!File.Exists(fileName))
        throw new FileNotFoundException(fileName);

    // First try to open the icalendar file as an appointment 
    // (not a calendar folder).
    object item = null;
    try
    {
        item = Application.Session.OpenSharedItem(fileName);
    }
    catch
    { }

    if (item != null)
    {
         // Display the item
         OutlookItem olItem = new OutlookItem(item);
         olItem.Display();
         return;
    }

    // If unsucessful in opening it as an item, 
    // try opening it as a folder
    Outlook.Folder importedFolder = null;
    try
    {
        importedFolder = Application.Session.OpenSharedFolder(
            fileName, Type.Missing, Type.Missing, Type.Missing) 
            as Outlook.Folder;
    }
    catch
    { }

    // If sucessful, open the folder in a new explorer window
    if (importedFolder != null)
    {
        Outlook.Explorer explorer =
            Application.Explorers.Add(importedFolder, 
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="f6077-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6077-114">See also</span></span>

- [<span data-ttu-id="f6077-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="f6077-115">Calendar</span></span>](calendar.md)

