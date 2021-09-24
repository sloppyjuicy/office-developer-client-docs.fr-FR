---
title: Accéder aux données propres à une solution stockées dans un message masqué dans un dossier
TOCTitle: Access solution-specific data stored as a hidden message in a folder
ms:assetid: bacf0562-1026-4c3b-87b0-4eaad5033592
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623414(v=office.15)
ms:contentKeyID: 55119861
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 03d2fd590f2b5c6eefdaec691a5ee25e9431f59f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549727"
---
# <a name="access-solution-specific-data-stored-as-a-hidden-message-in-a-folder"></a>Accéder aux données propres à une solution stockées dans un message masqué dans un dossier

Cet exemple montre comment utiliser l'objet [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) pour récupérer des données qui sont stockées sous forme de message masqué d'une classe de messages spécifique dans un dossier.

## <a name="example"></a>Exemple

L'objet **StorageItem** est généralement utilisé pour masquer les données spécifiques à une solution qui ne peuvent pas être affichées par programme. Dans un environnement Exchange, l'objet **StorageItem** est utilisé pour assurer l'itinérance des paramètres des solutions et garantir que ces paramètres sont disponibles en ligne et hors connexion. Vous pouvez affecter une classe de messages personnalisée à l'objet **StorageItem** ou identifier l'objet par son objet.

L'exemple de code suivant récupère les données XML qui sont stockées sous forme de message masqué dans le dossier Calendrier avec la classe de messages égale à IPM.Configuration.WorkHours.

L'objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) retourne le XML sous forme d'objet qui contient un flux d'octets et non comme une représentation sous forme de chaîne du XML. L'exemple de code utilise **System.Text.Encoding.Ascii.GetString** pour convertir le flux d'octets en chaîne.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

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


## <a name="see-also"></a>Voir aussi

- [Dossiers](folders.md)

