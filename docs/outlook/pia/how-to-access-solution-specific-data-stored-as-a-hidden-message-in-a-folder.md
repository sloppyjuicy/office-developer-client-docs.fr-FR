---
title: Accès aux données d’une solution stockée sous forme de message masqué dans un dossier
TOCTitle: Access solution-specific data stored as a hidden message in a folder
ms:assetid: bacf0562-1026-4c3b-87b0-4eaad5033592
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623414(v=office.15)
ms:contentKeyID: 55119861
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c64caf831f79ab61e5e3e0b9d712a511a7ba4f31
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537947"
---
# <a name="access-solution-specific-data-stored-as-a-hidden-message-in-a-folder"></a><span data-ttu-id="2c711-102">Accéder aux données propres à une solution stockées dans un message masqué dans un dossier</span><span class="sxs-lookup"><span data-stu-id="2c711-102">Access solution-specific data stored as a hidden message in a folder</span></span>

<span data-ttu-id="2c711-103">Cet exemple montre comment utiliser l'objet [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) pour récupérer des données qui sont stockées sous forme de message masqué d'une classe de messages spécifique dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="2c711-103">This example shows how to use the [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) object to retrieve data that is stored as a hidden message of a specific message class in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="2c711-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="2c711-104">Example</span></span>

<span data-ttu-id="2c711-p101">L'objet **StorageItem** est généralement utilisé pour masquer les données spécifiques à une solution qui ne peuvent pas être affichées par programme. Dans un environnement Exchange, l'objet **StorageItem** est utilisé pour assurer l'itinérance des paramètres des solutions et garantir que ces paramètres sont disponibles en ligne et hors connexion. Vous pouvez affecter une classe de messages personnalisée à l'objet **StorageItem** ou identifier l'objet par son objet.</span><span class="sxs-lookup"><span data-stu-id="2c711-p101">The **StorageItem** object is typically used to hide solution-specific data that cannot be displayed programmatically. In an Exchange environment, the **StorageItem** object is used to roam solution settings and ensure that these settings are available online and offline. You can assign a custom message class to the **StorageItem** object, or identify the object by subject.</span></span>

<span data-ttu-id="2c711-108">L'exemple de code suivant récupère les données XML qui sont stockées sous forme de message masqué dans le dossier Calendrier avec la classe de messages égale à IPM.Configuration.WorkHours.</span><span class="sxs-lookup"><span data-stu-id="2c711-108">The following code sample retrieves the XML data that is stored as a hidden message in the Calendar folder with the message class equal to IPM.Configuration.WorkHours.</span></span>

<span data-ttu-id="2c711-p102">L'objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) retourne le XML sous forme d'objet qui contient un flux d'octets et non comme une représentation sous forme de chaîne du XML. L'exemple de code utilise **System.Text.Encoding.Ascii.GetString** pour convertir le flux d'octets en chaîne.</span><span class="sxs-lookup"><span data-stu-id="2c711-p102">The [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object returns the XML as an object that contains a byte stream rather than a string representation of the XML. The code sample uses **System.Text.Encoding.Ascii.GetString** to convert the byte stream to a string.</span></span>

<span data-ttu-id="2c711-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="2c711-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="2c711-112">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="2c711-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="2c711-113">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="2c711-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Function GetWorkHoursXML() As String
    Try
        Dim storage As Outlook.StorageItem = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage( _
            "IPM.Configuration.WorkHours", _
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass)
        Dim pa As Outlook.PropertyAccessor = storage.PropertyAccessor
        ' PropertyAccessor will return a byte array for this property
        Dim rawXmlBytes As Byte() = CType(pa.GetProperty( _
            "http://schemas.microsoft.com/mapi/proptag/0x7C080102"), _
            Byte())
        ' Use Encoding to convert the array to a string
        Return System.Text.Encoding.ASCII.GetString(rawXmlBytes)
    Catch
        Return String.Empty
    End Try
End Function
```

```csharp
private string GetWorkHoursXML()
{
    try
    {
        Outlook.StorageItem storage =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage(
            "IPM.Configuration.WorkHours",
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass);
        Outlook.PropertyAccessor pa = storage.PropertyAccessor;
        // PropertyAccessor will return a byte array for this property
        byte[] rawXmlBytes = (byte[])pa.GetProperty(
            "http://schemas.microsoft.com/mapi/proptag/0x7C080102");
        // Use Encoding to convert the array to a string
        return System.Text.Encoding.ASCII.GetString(rawXmlBytes);
    }
    catch
    {
        return string.Empty;
    }
}
```


## <a name="see-also"></a><span data-ttu-id="2c711-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c711-114">See also</span></span>

- [<span data-ttu-id="2c711-115">Dossiers</span><span class="sxs-lookup"><span data-stu-id="2c711-115">Folders</span></span>](folders.md)

