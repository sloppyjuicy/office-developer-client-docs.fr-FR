---
title: Création d’un élément de courrier électronique avec un modèle de message
TOCTitle: Create a mail item by using a message template
ms:assetid: 7d1ffc3b-d1a7-46d1-adb9-ac41e67f626a
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623026(v=office.15)
ms:contentKeyID: 55119862
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cdd9654187685ceab1062fb4ae1882b2d48c68d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349538"
---
# <a name="create-a-mail-item-by-using-a-message-template"></a>Création d’un élément de courrier électronique avec un modèle de message

Cet exemple crée un élément de courrier à l’aide de la méthode [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\)).

## <a name="example"></a>Exemple

Cet exemple de code ouvre le fichier de modèle Ivy.oft, affecte un objet, puis enregistre le modèle dans le dossier Brouillons.

La méthode **CreateItemFromTemplate** est utile si un fichier de modèle de formulaire Outlook (.oft) que vous voulez utiliser comme modèle de message est stocké sur disque. Le fichier de modèle peut contenir du texte préformaté, du papier à lettres ou des images à inclure dans le message. Toutefois, si le fichier de modèle contient du code derrière le formulaire, le code du formulaire ne s'exécute pas.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateItemFromTemplate()
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderDrafts), Outlook.Folder)
    Dim mail As Outlook.MailItem = _
        CType(Application.CreateItemFromTemplate( _
        "c:\ivy.oft", folder), Outlook.MailItem)
    mail.Subject = "Congratulations"
    mail.Save()
End Sub
```


```csharp
private void CreateItemFromTemplate()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderDrafts) as Outlook.Folder;
    Outlook.MailItem mail =
        Application.CreateItemFromTemplate(
        @"c:\ivy.oft", folder) as Outlook.MailItem;
    mail.Subject = "Congratulations";
    mail.Save();
}
```

## <a name="see-also"></a>Voir aussi

- [Courrier](mail.md)

