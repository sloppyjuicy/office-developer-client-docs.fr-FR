---
title: Field2.AppendChunk Method (DAO)
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
ms.openlocfilehash: 2c21ea4943531f7b4ae32d49a2cb223802c68fb0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867383"
---
# <a name="field2appendchunk-method-dao"></a><span data-ttu-id="28032-102">Field2.AppendChunk Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="28032-102">Field2.AppendChunk Method (DAO)</span></span>


<span data-ttu-id="28032-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28032-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="28032-104">Ajoute des données issues d'une expression de chaîne à un objet **Field2** de type mémo ou binaire long dans un objet **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="28032-104">Appends data from a string expression to a Memo or Long Binary **Field2** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="28032-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28032-105">Syntax</span></span>

<span data-ttu-id="28032-106">*expression* . AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="28032-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="28032-107">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="28032-107">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="28032-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28032-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28032-109">Name</span><span class="sxs-lookup"><span data-stu-id="28032-109">Name</span></span></p></th>
<th><p><span data-ttu-id="28032-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="28032-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="28032-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="28032-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="28032-112">Description</span><span class="sxs-lookup"><span data-stu-id="28032-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28032-113">Val</span><span class="sxs-lookup"><span data-stu-id="28032-113">Val</span></span></p></td>
<td><p><span data-ttu-id="28032-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="28032-114">Required</span></span></p></td>
<td><p><span data-ttu-id="28032-115"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="28032-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="28032-116">Variable ou expression de type Variant (sous-type String) contenant les données à ajouter à l’objet <strong>Field2</strong>.</span><span class="sxs-lookup"><span data-stu-id="28032-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field2</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="28032-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="28032-117">Remarks</span></span>

<span data-ttu-id="28032-118">Vous pouvez utiliser les méthodes **AppendChunk** et **GetChunk** pour accéder à des sous-ensembles de données dans un champ de type mémo ou binaire long.</span><span class="sxs-lookup"><span data-stu-id="28032-118">You can use the **AppendChunk** and **GetChunk** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="28032-p101">Vous pouvez également les utiliser pour conserver de l'espace de chaîne lorsque vous utilisez des champs de type mémo et binaire long. Certaines opérations (la copie par exemple) font intervenir des chaînes temporaires. Si l'espace de chaîne est limité, il se peut que vous deviez utiliser des segments du champ au lieu du champ entier.</span><span class="sxs-lookup"><span data-stu-id="28032-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="28032-122">S'il n'existe aucun enregistrement actif lors de l'utilisation de la méthode **AppendChunk**, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="28032-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="28032-p102">L'opération <STRONG>AppendChunk</STRONG> initiale (après un appel à <STRONG><A href="recordset-edit-method-dao.md">Edit</A></STRONG> ou à <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> ) place simplement les données dans le champ en remplaçant les données existantes. Les appels à <STRONG>AppendChunk</STRONG> suivants au cours de la même session <STRONG>Edit</STRONG> ou <STRONG>AddNew</STRONG> ajoutent des données aux données existantes.</span><span class="sxs-lookup"><span data-stu-id="28032-p102">The initial <STRONG>AppendChunk</STRONG> operation (after an <STRONG><A href="recordset-edit-method-dao.md">Edit</A></STRONG> or <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> call) will simply place the data in the field, overwriting any existing data. Subsequent <STRONG>AppendChunk</STRONG> calls within the same <STRONG>Edit</STRONG> or <STRONG>AddNew</STRONG> session will then add to the existing data.</span></span></P>



## <a name="example"></a><span data-ttu-id="28032-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="28032-125">Example</span></span>

<span data-ttu-id="28032-p103">Cet exemple utilise les méthodes **AppendChunk** et **GetChunk** pour remplir un champ d'objet OLE avec des données issues d'un autre enregistrement, 32 Ko à la fois. Dans une application réelle, un utilisateur peut avoir recours à une procédure de ce type pour copier un enregistrement d'employé (y compris sa photo) d'une table à une autre. Dans le cadre de cet exemple, l'enregistrement est simplement recopié dans la même table. Notez que toute la manipulation des segments a lieu dans une seule séquence AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="28032-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
