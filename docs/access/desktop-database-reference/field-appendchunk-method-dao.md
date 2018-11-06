---
title: Méthode Field.AppendChunk (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 257dd342d0c0aa171d7961ab61a69da099497688
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997405"
---
# <a name="fieldappendchunk-method-dao"></a><span data-ttu-id="9572f-102">Méthode Field.AppendChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="9572f-102">Field.AppendChunk method (DAO)</span></span>

<span data-ttu-id="9572f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9572f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9572f-104">Ajoute des données issues d'une expression de chaîne à un objet **[Field](field-object-dao.md)** de type mémo ou binaire long dans un objet **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9572f-104">Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9572f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9572f-105">Syntax</span></span>

<span data-ttu-id="9572f-106">*expression* . AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="9572f-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="9572f-107">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="9572f-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9572f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9572f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9572f-109">Name</span><span class="sxs-lookup"><span data-stu-id="9572f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9572f-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="9572f-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9572f-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="9572f-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9572f-112">Description</span><span class="sxs-lookup"><span data-stu-id="9572f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9572f-113"><em>Val</em></span><span class="sxs-lookup"><span data-stu-id="9572f-113"><em>Val</em></span></span></p></td>
<td><p><span data-ttu-id="9572f-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9572f-114">Required</span></span></p></td>
<td><p><span data-ttu-id="9572f-115"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="9572f-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9572f-116">Variable ou expression de type Variant (sous-type String) contenant les données à ajouter à l’objet <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="9572f-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9572f-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="9572f-117">Remarks</span></span>

<span data-ttu-id="9572f-118">Vous pouvez utiliser les méthodes **AppendChunk** et **[GetChunk](field-getchunk-method-dao.md)** pour accéder à des sous-ensembles de données dans un champ de type mémo ou binaire long.</span><span class="sxs-lookup"><span data-stu-id="9572f-118">You can use the **AppendChunk** and **[GetChunk](field-getchunk-method-dao.md)** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="9572f-p101">Vous pouvez également les utiliser pour conserver de l'espace de chaîne lorsque vous utilisez des champs de type mémo et binaire long. Certaines opérations (la copie par exemple) font intervenir des chaînes temporaires. Si l'espace de chaîne est limité, il se peut que vous deviez utiliser des segments du champ au lieu du champ entier.</span><span class="sxs-lookup"><span data-stu-id="9572f-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="9572f-122">S'il n'existe aucun enregistrement actif lors de l'utilisation de la méthode **AppendChunk**, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="9572f-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="9572f-p102">L'opération **AppendChunk** initiale (après un appel à **[Edit](recordset-edit-method-dao.md)** ou à **[AddNew](recordset-addnew-method-dao.md)** ) place simplement les données dans le champ en remplaçant les données existantes. Les appels à **AppendChunk** suivants au cours de la même session **Edit** ou **AddNew** ajoutent des données aux données existantes.</span><span class="sxs-lookup"><span data-stu-id="9572f-p102">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data. Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="9572f-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="9572f-125">Example</span></span>

<span data-ttu-id="9572f-p103">Cet exemple utilise les méthodes **AppendChunk** et **GetChunk** pour remplir un champ d'objet OLE avec des données issues d'un autre enregistrement, 32 Ko à la fois. Dans une application réelle, un utilisateur peut avoir recours à une procédure de ce type pour copier un enregistrement d'employé (y compris sa photo) d'une table à une autre. Dans le cadre de cet exemple, l'enregistrement est simplement recopié dans la même table. Notez que toute la manipulation des segments a lieu dans une seule séquence AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="9572f-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
