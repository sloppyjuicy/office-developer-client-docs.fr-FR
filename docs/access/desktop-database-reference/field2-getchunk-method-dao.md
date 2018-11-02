---
title: Méthode Field2.GetChunk (DAO)
TOCTitle: GetChunk Method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09660c472a6fd799c111214dafe3266cdec9eced
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926646"
---
# <a name="field2getchunk-method-dao"></a>Méthode Field2.GetChunk (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie tout ou partie du contenu d’un objet de **type Memo** ou **Long BinaryField2** de la collection **[Fields](fields-collection-dao.md)** d’un objet **[Recordset](recordset-object-dao.md)** .

## <a name="syntax"></a>Syntaxe

*expression* . GetChunk (***décalage***, ***octets***)

*expression* Variable qui représente un objet **Field2** .

### <a name="parameters"></a>Paramètres

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
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Offset</p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Entier long</strong></p></td>
<td><p>Nombre d'octets à ignorer avant que la copie ne commence.</p></td>
</tr>
<tr class="even">
<td><p>Octets</p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Entier long</strong></p></td>
<td><p>Nombre d'octets que vous souhaitez renvoyer.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Variant

## <a name="remarks"></a>Remarques

Les octets renvoyés par **GetChunk** sont affectés à une variable. Utilisez **GetChunk** pour renvoyer une partie de la valeur totale des données à la fois. Vous pouvez avoir recours à **[AppendChunk](field-appendchunk-method-dao.md)** pour reconstituer les différentes parties.

Si le décalage est égal à 0, **GetChunk** commence la copie à partir du premier octet du champ.

Si la valeur du paramètre NbOctets est supérieur au nombre d’octets dans le champ, **GetChunk** renvoie le nombre réel d’octets restant dans le champ.


> [!NOTE]
> <P>[!REMARQUE] Utilisez un champ de type <STRONG>Memo</STRONG> pour du texte et placez les données binaires uniquement dans des champs de type <STRONG>Long Binary</STRONG>. Sinon, vous n'obtiendrez pas les résultats escomptés.</P>



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
