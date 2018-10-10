---
title: Field.FieldSize Property (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4de733dd88be212779d3ab9d9b562d4741492a87
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471922"
---
# <a name="fieldfieldsize-property-dao"></a><span data-ttu-id="46dd5-102">Field.FieldSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="46dd5-102">Field.FieldSize Property (DAO)</span></span>


<span data-ttu-id="46dd5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="46dd5-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="46dd5-104">Renvoie le nombre d'octets utilisés dans la base de données (plutôt que la mémoire) d'un objet **[Field](field-object-dao.md)** de type Mémo ou Binaire long de la collection **[Fields](fields-collection-dao.md)** d'un objet **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="46dd5-104">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="46dd5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46dd5-105">Syntax</span></span>

<span data-ttu-id="46dd5-106">*expression* . Taille du champ</span><span class="sxs-lookup"><span data-stu-id="46dd5-106">*expression* .FieldSize</span></span>

<span data-ttu-id="46dd5-107">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="46dd5-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="46dd5-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="46dd5-108">Remarks</span></span>

<span data-ttu-id="46dd5-109">Utilisez **FieldSize** avec les méthodes **[AppendChunk](field-appendchunk-method-dao.md)** et **[GetChunk](field-getchunk-method-dao.md)** pour manipulater des champs de grande taille.</span><span class="sxs-lookup"><span data-stu-id="46dd5-109">You can use **FieldSize** with the **[AppendChunk](field-appendchunk-method-dao.md)** and **[GetChunk](field-getchunk-method-dao.md)** methods to manipulate large fields.</span></span>

<span data-ttu-id="46dd5-110">Comme la taille d'un champ Valeur binaire longue ou Mémo peut dépasser 64K, il convient de définir la valeur renvoyée par **FieldSize** sur une variable suffisamment grande pour stocker la variable **Long**.</span><span class="sxs-lookup"><span data-stu-id="46dd5-110">Because the size of a Long Binary or Memo field can exceed 64K, you should assign the value returned by **FieldSize** to a variable large enough to store a **Long** variable.</span></span>

<span data-ttu-id="46dd5-111">Pour déterminer la taille d'un objet **Field** de type autre que Mémo et Binaire long, utilisez la propriété **[Size](field-size-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="46dd5-111">To determine the size of a **Field** object other than Memo and Long Binary types, use the **[Size](field-size-property-dao.md)** property.</span></span>

  - <span data-ttu-id="46dd5-112">Si le serveur de base de données ou le pilote ODBC ne prend pas en charge les curseurs côté serveur.</span><span class="sxs-lookup"><span data-stu-id="46dd5-112">If the database server or ODBC driver does not support server-side cursors.</span></span>

  - <span data-ttu-id="46dd5-113">Si vous utilisez la bibliothèque de curseurs ODBC (en d'autres termes, la propriété **DefaultCursorDriver** est définie sur **dbUseODBC** ou sur **dbUseDefault** lorsque le serveur ne prend pas en charge les curseurs côté serveur).</span><span class="sxs-lookup"><span data-stu-id="46dd5-113">If you are using the ODBC cursor library (that is, the **DefaultCursorDriver** property is set to **dbUseODBC**, or to **dbUseDefault** when the server does not support server-side cursors).</span></span>

  - <span data-ttu-id="46dd5-114">Si vous utilisez une requête sans curseur (en d'autres termes, la propriété **DefaultCursorDriver** est définie sur **dbUseNoCursor**).</span><span class="sxs-lookup"><span data-stu-id="46dd5-114">If you are using a cursorless query (that is, the **DefaultCursorDriver** property is set to **dbUseNoCursor**).</span></span>

<span data-ttu-id="46dd5-p101">La propriété **FieldSize** et les fonctions VBA **Len()** ou **LenB()** peuvent renvoyer des valeurs différentes pour la longueur de la même chaîne. Les chaînes sont stockées dans une base de données Microsoft Access dans un formulaire de jeu de données à plusieurs octets (MBCS), mais exposées via VBA au format Unicode. Par conséquent, la fonction **Len()** renvoie toujours le nombre de caractères, **LenB** renvoie toujours le nombre de caractères X 2 (Unicode utilise deux octets pour chaque caractère), mais **FieldSize** renvoie une valeur intermédiaire si la chaîne a des caractères MBCS. Par exemple, pour une chaîne constituée de trois caractères normaux et de deux caractères MBCS, **Len()** renvoie 5, **LenB()** renvoie 10 et **FieldSize** renvoie 7, la somme de 1 pour chaque caractère normal et 2 pour chaque caractère MBCS.</span><span class="sxs-lookup"><span data-stu-id="46dd5-p101">The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string. Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format. As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters. For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.</span></span>

## <a name="example"></a><span data-ttu-id="46dd5-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="46dd5-119">Example</span></span>

<span data-ttu-id="46dd5-120">Cet exemple utilise la propriété **FieldSize** pour répertorier le nombre d'octets utilisés par les objets Memo et Long Binary Field de deux tables différentes.</span><span class="sxs-lookup"><span data-stu-id="46dd5-120">This example uses the **FieldSize** property to list the number of bytes used by the Memo and Long Binary Field objects in two different tables.</span></span>

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

<br/>

<span data-ttu-id="46dd5-p102">Cet exemple utilise les méthodes **AppendChunk** et **GetChunk** pour remplir un champ d'objet OLE avec des données issues d'un autre enregistrement, 32 Ko à la fois. Dans une application réelle, un utilisateur peut avoir recours à une procédure de ce type pour copier un enregistrement d'employé (y compris sa photo) d'une table à une autre. Dans le cadre de cet exemple, l'enregistrement est simplement recopié dans la même table. Notez que toute la manipulation des segments a lieu dans une seule séquence AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="46dd5-p102">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
