---
title: Méthode Field.GetChunk (DAO)
TOCTitle: GetChunk Method
ms:assetid: b8984e79-54f7-8052-85a3-d12033daf7a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822448(v=office.15)
ms:contentKeyID: 48547328
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052871
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c7eabceb1f7c130e349428aeb6b2dc079fe4319d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703747"
---
# <a name="fieldgetchunk-method-dao"></a>Méthode Field.GetChunk (DAO)

**S’applique à**: Access 2013, Office 2013

Renvoie tout ou partie du contenu d'un objet ****Field**** de type [Memo](field-object-dao.md) ou **Long Binary** appartenant à la collection **[Fields](fields-collection-dao.md)** d'un objet **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . GetChunk (***décalage***, ***octets***)

*expression* Variable qui représente un objet **Field** .

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
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Offset</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Nombre d'octets à ignorer avant que la copie ne commence.</p></td>
</tr>
<tr class="even">
<td><p><em>Octets</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Nombre d'octets que vous souhaitez renvoyer.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Variant

## <a name="remarks"></a>Remarques

Les octets renvoyés par **GetChunk** sont affectés à une variable. Utilisez **GetChunk** pour renvoyer une partie de la valeur totale des données à la fois. Vous pouvez avoir recours à **[AppendChunk](field-appendchunk-method-dao.md)** pour reconstituer les différentes parties.

Si le décalage est égal à 0, **GetChunk** commence la copie à partir du premier octet du champ.

Si la valeur du paramètre NbOctets est supérieur au nombre d’octets dans le champ, **GetChunk** renvoie le nombre réel d’octets restant dans le champ.

> [!NOTE]
> [!REMARQUE] Utilisez un champ de type **Memo** pour du texte et placez les données binaires uniquement dans des champs de type **Long Binary**. Sinon, vous n'obtiendrez pas les résultats escomptés.

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
     
    Function CopyLargeField(fldSource As Field, _ 
     fldDestination As Field) 
     
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
