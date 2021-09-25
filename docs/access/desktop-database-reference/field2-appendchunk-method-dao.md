---
title: Field2.AppendChunk, méthode (DAO)
TOCTitle: AppendChunk Method
ms:assetid: 540cd02d-1fc6-81d1-ac08-1e3df72a7208
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194088(v=office.15)
ms:contentKeyID: 48544886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052867
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 26b11bad02c8943dba71f4d41486a78d3ec2eb30
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581279"
---
# <a name="field2appendchunk-method-dao"></a>Field2.AppendChunk, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Ajoute des données issues d'une expression de chaîne à un objet **Field2** de type mémo ou binaire long dans un objet **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*.* AppendChunk(***Val***)

*expression* une variable qui représente une **champ2** objet.

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
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Val</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Variable ou expression de type Variant (sous-type String) contenant les données à ajouter à l’objet <strong>Field2</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Vous pouvez utiliser les méthodes **AppendChunk** et **GetChunk** pour accéder à des sous-ensembles de données dans un champ de type mémo ou binaire long.

Vous pouvez également les utiliser pour conserver de l'espace de chaîne lorsque vous utilisez des champs de type mémo et binaire long. Certaines opérations (la copie par exemple) font intervenir des chaînes temporaires. Si l'espace de chaîne est limité, il se peut que vous deviez utiliser des segments du champ au lieu du champ entier.

S'il n'existe aucun enregistrement actif lors de l'utilisation de la méthode **AppendChunk**, une erreur se produit.

> [!NOTE]
> L'opération **AppendChunk** initiale (après un appel à **[Edit](recordset-edit-method-dao.md)** ou à **[AddNew](recordset-addnew-method-dao.md)** ) place simplement les données dans le champ en remplaçant les données existantes. Les appels à **AppendChunk** suivants au cours de la même session **Edit** ou **AddNew** ajoutent des données aux données existantes.

## <a name="example"></a>Exemple

Cet exemple utilise les méthodes **AppendChunk** et **GetChunk** pour remplir un champ d'objet OLE avec des données issues d'un autre enregistrement, 32 Ko à la fois. Dans une application réelle, un utilisateur peut avoir recours à une procédure de ce type pour copier un enregistrement d'employé (y compris sa photo) d'une table à une autre. Dans le cadre de cet exemple, l'enregistrement est simplement recopié dans la même table. Notez que toute la manipulation des segments a lieu dans une seule séquence AddNew-Update.

```vb
    Sub AppendChunkX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim rstEmployees2 As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Open two recordsets from the Employees table. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenDynaset) 
       Set rstEmployees2 = rstEmployees.Clone 
     
       ' Add a new record to the first Recordset and copy the  
       ' data from a record in the second Recordset. 
       With rstEmployees 
          .AddNew 
          !FirstName = rstEmployees2!FirstName 
          !LastName = rstEmployees2!LastName 
          CopyLargeField rstEmployees2!Photo, !Photo 
          .Update 
     
          ' Delete new record because this is a demonstration. 
          .Bookmark = .LastModified 
          .Delete 
          .Close 
       End With 
     
       rstEmployees2.Close 
       dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field2, _ 
       fldDestination As Field2) 
     
       ' Set size of chunk in bytes. 
       Const conChunkSize = 32768 
     
       Dim lngOffset As Long 
       Dim lngTotalSize As Long 
       Dim strChunk As String 
     
       ' Copy the photo from one Recordset to the other in 32K  
       ' chunks until the entire field is copied. 
       lngTotalSize = fldSource.FieldSize 
       Do While lngOffset < lngTotalSize 
          strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
          fldDestination.AppendChunk strChunk 
          lngOffset = lngOffset + conChunkSize 
       Loop 
     
    End Function
```
