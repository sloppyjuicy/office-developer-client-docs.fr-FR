---
title: Field2. Required, propriété (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6b1950c8a864fbf23bee26be89e07e49357840b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292719"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="a5ac9-102">Field2. Required, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="a5ac9-102">Field2.Required property (DAO)</span></span>


<span data-ttu-id="a5ac9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5ac9-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a5ac9-104">Définit ou renvoie une valeur qui indique si un objet **Field2** requiert une valeur non nulle.</span><span class="sxs-lookup"><span data-stu-id="a5ac9-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5ac9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5ac9-105">Syntax</span></span>

<span data-ttu-id="a5ac9-106">*expression* . Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a5ac9-106">*expression* .Required</span></span>

<span data-ttu-id="a5ac9-107">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="a5ac9-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5ac9-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5ac9-108">Remarks</span></span>

<span data-ttu-id="a5ac9-109">Pour un objet **Field2** pas encore ajouté à la collection **Fields**, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a5ac9-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="a5ac9-110">La disponibilité de la propriété **Required** dépend de l'objet contenant la collection **[Fields](fields-collection-dao.md)**, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a5ac9-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5ac9-111">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="a5ac9-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="a5ac9-112">Alors Required est</span><span class="sxs-lookup"><span data-stu-id="a5ac9-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5ac9-113">objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a5ac9-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a5ac9-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5ac9-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5ac9-115">objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a5ac9-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a5ac9-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5ac9-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5ac9-117">objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a5ac9-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a5ac9-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a5ac9-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5ac9-119">objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="a5ac9-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a5ac9-120">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="a5ac9-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5ac9-121">objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a5ac9-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a5ac9-122">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="a5ac9-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5ac9-p101">Vous pouvez utiliser la propriété **Required** avec les propriétés **AllowZeroLength**, **ValidateOnSet** ou **ValidationRule** pour déterminer la validité du paramètre de propriété **Value** pour cet objet **Field2**. Si la propriété **Required** est définie sur **False**, le champ peut contenir des valeurs de type **null** et des valeurs répondant aux conditions spécifiées par les paramètres de propriété **AllowZeroLength** et **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="a5ac9-p101">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="a5ac9-p102">[!REMARQUE] Lorsque vous définissez cette propriété pour un objet **Index** ou **Field2**, définissez-la pour l'objet **Field2**. La validité du paramètre de propriété d'un objet **Field2** est vérifiée avant celle d'un objet **Index**.</span><span class="sxs-lookup"><span data-stu-id="a5ac9-p102">When you can set this property for either an **Index** object or a **Field2** object, set it for the **Field2** object. The validity of the property setting for a **Field2** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="a5ac9-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5ac9-127">Example</span></span>

<span data-ttu-id="a5ac9-p103">Cet exemple utilise la propriété **Required** pour signaler les champs de trois tables différentes à renseigner obligatoirement pour ajouter un nouvel enregistrement. La fonction RequiredOutput est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a5ac9-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

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

