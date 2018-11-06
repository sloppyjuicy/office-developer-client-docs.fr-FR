---
title: Properties, collection (DAO)
TOCTitle: Properties collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0cd2198d0578c6ec42e4bf800d95e1d7afe22786
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998342"
---
# <a name="properties-collection-dao"></a>Properties, collection (DAO)

**S’applique à**: Access 2013, Office 2013

Une collection **Properties** contient tous les objets **[Property](property-object-dao.md)** d'une instance spécifique d'un objet.

## <a name="remarks"></a>Remarques

Tous les objets DAO, à l'exception des objets **Connection** et **Error**, contiennent une collection **Properties**, laquelle est dotée d'un certain nombre d'objets **Property** intégrés. Ces objets **Property** (souvent appelés simplement propriétés) caractérisent de manière unique cette instance de l'objet.

Outre les propriétés intégrées, vous pouvez également créer et ajouter vos propres propriétés. Pour ajouter une propriété personnalisée à une instance existante d'un objet, il convient d'abord d'en définir les caractéristiques à l'aide de la méthode **CreateProperty**, puis de l'ajouter à la collection à l'aide de la méthode **Append**. Le référencement d'un objet **Property** défini par l'utilisateur qui n'a pas encore été ajouté à une collection **Properties** entraîne une erreur. Tout comme l'ajout d'un objet **Property** défini par l'utilisateur à une collection **Properties** comptant déjà un objet **Property** avec le même nom.

Vous pouvez utiliser la méthode **Delete** pour supprimer des propriétés personnalisées de la collection **Properties** mais vous ne pouvez pas supprimer les propriétés intégrées.

> [!NOTE]
> [!REMARQUE] Un objet **Property** défini par l'utilisateur est associé uniquement à l'instance spécifique d'un objet. La propriété n'est pas définie pour toutes les instances d'objets du type sélectionné.

Pour faire référence à un objet **Property** intégré d'une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des syntaxes suivantes :

- objet. **Propriétés** (0)

- objet. **Propriétés** (« nom »)

- objet. **Propriétés** \! \[nom\]

Pour une propriété intégrée, vous pouvez également utiliser la syntaxe suivante :

- objet.Name

> [!NOTE]
> Pour une propriété définie par l’utilisateur, vous devez utiliser l’objet complet. **Propriétés** syntaxe (« nom »).

Avec les mêmes formes de syntaxe, vous pouvez également faire référence à la propriété **Value** d'un objet **Property**. Le contexte de la référence déterminera si vous faites référence à l'objet **Property** lui-même ou à la propriété **Value** de l'objet **Property**.

## <a name="example"></a>Exemple

Cet exemple crée une propriété définie par l'utilisateur pour la base de données active, définit ses propriétés **Type** et **Value** et l'ajoute à la collection **Properties** de la base de données. Il énumère ensuite toutes les propriétés de la base de données.

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

Cet exemple tente de définir la valeur d'une propriété définie par l'utilisateur. Si la propriété n'existe pas, il utilise la méthode **CreateProperty** pour créer la nouvelle propriété et en définir la valeur. La procédure SetProperty est requise pour exécuter cette opération.

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
