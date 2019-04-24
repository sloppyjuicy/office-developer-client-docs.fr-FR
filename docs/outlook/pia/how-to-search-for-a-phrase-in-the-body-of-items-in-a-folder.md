---
title: Recherche dans un dossier d’une expression employée dans le corps des éléments
TOCTitle: Search for a phrase in the body of items in a folder
ms:assetid: 2c9f3b5f-ed91-4a07-b247-8f89f00cbc68
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644806(v=office.15)
ms:contentKeyID: 55119924
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dc8e0fb2b82ae9660e292a6ec1dea70e82fe36ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316029"
---
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a>Recherche dans un dossier d’une expression employée dans le corps des éléments

Cet exemple recherche la chaîne « office » dans le corps des éléments de la boîte de réception.

## <a name="example"></a>Exemple

Cet exemple de code utilise une syntaxe DASL (DAV Searching and Locating) pour spécifier une requête. Pour construire le filtre, l’exemple de code vérifie d’abord si la recherche instantanée est activée dans la banque par défaut afin de déterminer s’il faut utiliser le mot clé **ci\_phrasematch** pour une correspondance de phrase exacte de « office » dans le corps de l’élément, ou le mot clé **like** pour trouver toute occurrence de « office » comme chaîne ou sous-chaîne exacte dans le corps de l’élément. L’exemple applique ensuite le filtre à la méthode [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) sur la Boîte de réception et obtient les résultats dans un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)). L’exemple de code affiche ensuite l’objet de chaque élément renvoyé dans l’objet **Table**.

L’exemple de code spécifie la propriété **Body** en utilisant la représentation d’espace de noms urn:schemas:httpmail:textdescription.

La syntaxe à employer pour utiliser le mot clé **ci\_phrasematch** est la suivante :

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

La syntaxe à employer pour utiliser le mot clé **like** pour la correspondance de préfixes est la suivante :

`<PropertySchemaName> like <Token>%`

La syntaxe à employer pour utiliser le mot clé **like** pour la correspondance de sous-chaînes est la suivante :

`<PropertySchemaName> like %<Token>%`

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchBody()
    Dim filter As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " ci_phrasematch 'office'"
    Else
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " like '%office%'"
    End If
    Dim table As Outlook.Table = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
        filter, Outlook.OlTableContents.olUserItems)
    While Not (table.EndOfTable)
        Dim row As Outlook.Row = table.GetNextRow()
        Debug.WriteLine(row("Subject"))
    End While
End Sub
```


```csharp
private void DemoSearchBody()
{
    string filter;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " ci_phrasematch 'office'";
    }
    else
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " like '%office%'";
    }
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

