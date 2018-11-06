---
title: Méthode TableDef.CreateIndex (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 429b64ae3909e320433b34d1426e396926fafba7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997475"
---
# <a name="tabledefcreateindex-method-dao"></a>Méthode TableDef.CreateIndex (DAO)

**S’applique à**: Access 2013, Office 2013 

Crée un nouvel objet **[Index](index-object-dao.md)** (Espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . CreateIndex (***nom***)

*expression* Variable qui représente un objet **TableDef** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Type <strong>String</strong> qui identifie de façon unique le nouvel objet <strong>Index</strong>. Consultez la propriété <strong>Name</strong> pour plus d'informations sur les noms d'objets <strong>Index</strong> valides.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Index

## <a name="remarks"></a>Remarques

Vous pouvez utiliser la méthode **CreateIndex** afin de créer un un objet **Index** pour un objet **TableDef**. Si vous ne spécifiez pas le nom facultatif **CreateIndex**, vous pouvez utiliser une instruction d’affectation appropriée pour définir ou redéfinir la propriété **Name** avant d’ajouter le nouvel objet à une collection. Après l'ajout de l'objet, il n'est pas toujours possible de définir sa propriété **Name**, selon le type d'objet qui contient la collection **Indexes**. Pour plus d'informations, consultez la rubrique de la propriété **Name**.

Si le nom fait référence à un objet qui est déjà membre de la collection, une erreur d’exécution se produit lorsque vous utilisez la méthode **[Append](fields-append-method-dao.md)** .

Pour supprimer un objet **Index** d'une collection, appelez la méthode **[Delete](fields-delete-method-dao.md)** sur la collection.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **CreateIndex** pour créer deux nouveaux objets **Index** et les ajouter à la collection **Indexes** de l'objet **TableDef** Employees. Il énumère ensuite la collection Indexes de l'objet **TableDef**, la collection **Fields** des nouveaux objets **Index**, et la collection Properties des nouveaux objets **Index**. La fonction CreateIndexOutput est requise pour exécuter cette opération.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
