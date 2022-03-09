---
title: Field.FieldSize, propriété (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5b0dca69ea925a72f7b5f4d108fec5bca1c30600
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464233"
---
# <a name="fieldfieldsize-property-dao"></a>Field.FieldSize, propriété (DAO)


**S’applique à** : Access 2013, Office 2013


Renvoie le nombre d'octets utilisés dans la base de données (plutôt que la mémoire) d'un objet **[Field](field-object-dao.md)** de type Mémo ou Binaire long de la collection **[Fields](fields-collection-dao.md)** d'un objet **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*.* FieldSize

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

Utilisez **FieldSize** avec les méthodes **[AppendChunk](field-appendchunk-method-dao.md)** et **[GetChunk](field-getchunk-method-dao.md)** pour manipulater des champs de grande taille.

Comme la taille d'un champ Valeur binaire longue ou Mémo peut dépasser 64K, il convient de définir la valeur renvoyée par **FieldSize** sur une variable suffisamment grande pour stocker la variable **Long**.

Pour déterminer la taille d'un objet **Field** de type autre que Mémo et Binaire long, utilisez la propriété **[Size](field-size-property-dao.md)**.

  - Si le serveur de base de données ou le pilote ODBC ne prend pas en charge les curseurs côté serveur.

  - Si vous utilisez la bibliothèque de curseurs ODBC (en d'autres termes, la propriété **DefaultCursorDriver** est définie sur **dbUseODBC** ou sur **dbUseDefault** lorsque le serveur ne prend pas en charge les curseurs côté serveur).

  - Si vous utilisez une requête sans curseur (en d'autres termes, la propriété **DefaultCursorDriver** est définie sur **dbUseNoCursor**).

La propriété **FieldSize** et les fonctions VBA **Len()** ou **LenB()** peuvent renvoyer des valeurs différentes pour la longueur de la même chaîne. Les chaînes sont stockées dans une base de données Microsoft Access dans un formulaire de jeu de données à plusieurs octets (MBCS), mais exposées via VBA au format Unicode. Par conséquent, la fonction **Len()** renvoie toujours le nombre de caractères, **LenB** renvoie toujours le nombre de caractères X 2 (Unicode utilise deux octets pour chaque caractère), mais **FieldSize** renvoie une valeur intermédiaire si la chaîne a des caractères MBCS. Par exemple, pour une chaîne constituée de trois caractères normaux et de deux caractères MBCS, **Len()** renvoie 5, **LenB()** renvoie 10 et **FieldSize** renvoie 7, la somme de 1 pour chaque caractère normal et 2 pour chaque caractère MBCS.

## <a name="example"></a>Exemple

Cet exemple utilise la propriété **FieldSize** pour répertorier le nombre d'octets utilisés par les objets Memo et Long Binary Field de deux tables différentes.

```vb
    Sub FieldSizeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenDynaset) 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     Debug.Print _ 
     "Field sizes from records in Categories table" 
     
     With rstCategories 
     Debug.Print " CategoryName - " & _ 
     "Description (bytes) - Picture (bytes)" 
     
     ' Enumerate the Categories Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !CategoryName & " - " & _ 
     !Description.FieldSize & " - " & _ 
     !Picture.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     Debug.Print "Field sizes from records in Employees table" 
     
     With rstEmployees 
     Debug.Print " LastName - Notes (bytes) - " & _ 
     "Photo (bytes)" 
     
     ' Enumerate the Employees Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & " - " & _ 
     !Notes.FieldSize & " - " & !Photo.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```


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
