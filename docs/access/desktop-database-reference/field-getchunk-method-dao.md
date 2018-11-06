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
ms.openlocfilehash: f8d245223549d51c49e769eedd0b92bb335357cf
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996992"
---
# <a name="fieldgetchunk-method-dao"></a><span data-ttu-id="5b2fa-102">Méthode Field.GetChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="5b2fa-102">Field.GetChunk method (DAO)</span></span>

<span data-ttu-id="5b2fa-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b2fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b2fa-104">Renvoie tout ou partie du contenu d'un objet \*\*\*\*Field\*\*\*\* de type [Memo](field-object-dao.md) ou **Long Binary** appartenant à la collection **[Fields](fields-collection-dao.md)** d'un objet **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-104">Returns all or a portion of the contents of a **Memo** or **Long Binary** **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b2fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b2fa-105">Syntax</span></span>

<span data-ttu-id="5b2fa-106">*expression* . GetChunk (***décalage***, ***octets***)</span><span class="sxs-lookup"><span data-stu-id="5b2fa-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="5b2fa-107">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="5b2fa-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b2fa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b2fa-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b2fa-109">Name</span><span class="sxs-lookup"><span data-stu-id="5b2fa-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5b2fa-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="5b2fa-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5b2fa-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="5b2fa-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="5b2fa-112">Description</span><span class="sxs-lookup"><span data-stu-id="5b2fa-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b2fa-113"><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="5b2fa-113"><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="5b2fa-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5b2fa-114">Required</span></span></p></td>
<td><p><span data-ttu-id="5b2fa-115"><strong>Entier long</strong></span><span class="sxs-lookup"><span data-stu-id="5b2fa-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="5b2fa-116">Nombre d'octets à ignorer avant que la copie ne commence.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b2fa-117"><em>Octets</em></span><span class="sxs-lookup"><span data-stu-id="5b2fa-117"><em>Bytes</em></span></span></p></td>
<td><p><span data-ttu-id="5b2fa-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5b2fa-118">Required</span></span></p></td>
<td><p><span data-ttu-id="5b2fa-119"><strong>Entier long</strong></span><span class="sxs-lookup"><span data-stu-id="5b2fa-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="5b2fa-120">Nombre d'octets que vous souhaitez renvoyer.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="5b2fa-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5b2fa-121">Return value</span></span>

<span data-ttu-id="5b2fa-122">Variant</span><span class="sxs-lookup"><span data-stu-id="5b2fa-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="5b2fa-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="5b2fa-123">Remarks</span></span>

<span data-ttu-id="5b2fa-p101">Les octets renvoyés par **GetChunk** sont affectés à une variable. Utilisez **GetChunk** pour renvoyer une partie de la valeur totale des données à la fois. Vous pouvez avoir recours à **[AppendChunk](field-appendchunk-method-dao.md)** pour reconstituer les différentes parties.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-p101">The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="5b2fa-127">Si le décalage est égal à 0, **GetChunk** commence la copie à partir du premier octet du champ.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="5b2fa-128">Si la valeur du paramètre NbOctets est supérieur au nombre d’octets dans le champ, **GetChunk** renvoie le nombre réel d’octets restant dans le champ.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>

> [!NOTE]
> <span data-ttu-id="5b2fa-p102">[!REMARQUE] Utilisez un champ de type **Memo** pour du texte et placez les données binaires uniquement dans des champs de type **Long Binary**. Sinon, vous n'obtiendrez pas les résultats escomptés.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-p102">Use a **Memo** field for text, and put binary data only in **Long Binary** fields. Doing otherwise will cause undesirable results.</span></span>

## <a name="example"></a><span data-ttu-id="5b2fa-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="5b2fa-131">Example</span></span>

<span data-ttu-id="5b2fa-p103">Cet exemple utilise les méthodes **AppendChunk** et **GetChunk** pour remplir un champ d'objet OLE avec des données issues d'un autre enregistrement, 32 Ko à la fois. Dans une application réelle, un utilisateur peut avoir recours à une procédure de ce type pour copier un enregistrement d'employé (y compris sa photo) d'une table à une autre. Dans le cadre de cet exemple, l'enregistrement est simplement recopié dans la même table. Notez que toute la manipulation des segments a lieu dans une seule séquence AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
