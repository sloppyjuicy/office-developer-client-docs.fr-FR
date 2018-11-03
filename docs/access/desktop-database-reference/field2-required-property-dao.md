---
title: Propriété Field2.Required (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf5e459773cd0fa0976704834b1b73467fc75294
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937406"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="02a31-102">Propriété Field2.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="02a31-102">Field2.Required property (DAO)</span></span>


<span data-ttu-id="02a31-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02a31-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="02a31-104">Définit ou renvoie une valeur qui indique si un objet **Field2** requiert une valeur non nulle.</span><span class="sxs-lookup"><span data-stu-id="02a31-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02a31-105">Syntax</span></span>

<span data-ttu-id="02a31-106">*expression* . Obligatoire</span><span class="sxs-lookup"><span data-stu-id="02a31-106">*expression* .Required</span></span>

<span data-ttu-id="02a31-107">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="02a31-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="02a31-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="02a31-108">Remarks</span></span>

<span data-ttu-id="02a31-109">Pour un objet **Field2** pas encore ajouté à la collection **Fields**, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="02a31-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="02a31-110">La disponibilité de la propriété **Required** dépend de l'objet contenant la collection **[Fields](fields-collection-dao.md)**, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="02a31-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02a31-111">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="02a31-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="02a31-112">Alors Required est</span><span class="sxs-lookup"><span data-stu-id="02a31-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02a31-113">							objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="02a31-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="02a31-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="02a31-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a31-115">							objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="02a31-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="02a31-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02a31-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02a31-117">							objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="02a31-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="02a31-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="02a31-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02a31-119">							objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="02a31-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="02a31-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="02a31-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02a31-121">							objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="02a31-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="02a31-122">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="02a31-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02a31-p101">Vous pouvez utiliser la propriété **Required** avec les propriétés **AllowZeroLength**, **ValidateOnSet** ou **ValidationRule** pour déterminer la validité du paramètre de propriété **Value** pour cet objet **Field2**. Si la propriété **Required** est définie sur **False**, le champ peut contenir des valeurs de type **null** et des valeurs répondant aux conditions spécifiées par les paramètres de propriété **AllowZeroLength** et **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="02a31-p101">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="02a31-p102">[!REMARQUE] Lorsque vous définissez cette propriété pour un objet **Index** ou **Field2**, définissez-la pour l'objet **Field2**. La validité du paramètre de propriété d'un objet **Field2** est vérifiée avant celle d'un objet **Index**.</span><span class="sxs-lookup"><span data-stu-id="02a31-p102">When you can set this property for either an **Index** object or a **Field2** object, set it for the **Field2** object. The validity of the property setting for a **Field2** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="02a31-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="02a31-127">Example</span></span>

<span data-ttu-id="02a31-p103">Cet exemple utilise la propriété **Required** pour signaler les champs de trois tables différentes à renseigner obligatoirement pour ajouter un nouvel enregistrement. La fonction RequiredOutput est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="02a31-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

