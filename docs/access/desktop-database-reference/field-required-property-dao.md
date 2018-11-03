---
title: Propriété Field.Required (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6fbf95e02c9945558d70fff35f12a73ce0dee45e
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937315"
---
# <a name="fieldrequired-property-dao"></a><span data-ttu-id="df48d-102">Propriété Field.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="df48d-102">Field.Required property (DAO)</span></span>


<span data-ttu-id="df48d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df48d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df48d-104">Définit ou renvoie une valeur qui indique si un objet **[Field](field-object-dao.md)** requiert une valeur non Null.</span><span class="sxs-lookup"><span data-stu-id="df48d-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="df48d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df48d-105">Syntax</span></span>

<span data-ttu-id="df48d-106">*expression* . Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df48d-106">*expression* .Required</span></span>

<span data-ttu-id="df48d-107">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="df48d-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="df48d-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="df48d-108">Remarks</span></span>

<span data-ttu-id="df48d-109">Pour un objet **Field** qui n'a pas encore été ajouté à la collection **Fields**, cette propriété est en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="df48d-109">For a **Field** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="df48d-110">La disponibilité de la propriété **Required** dépend de l'objet qui contient la collection [Fields](fields-collection-dao.md), comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="df48d-110">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df48d-111">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="df48d-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="df48d-112">Alors Required est</span><span class="sxs-lookup"><span data-stu-id="df48d-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df48d-113">							objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="df48d-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="df48d-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="df48d-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df48d-115">							objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="df48d-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="df48d-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df48d-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df48d-117">							objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="df48d-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="df48d-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df48d-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df48d-119">							objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="df48d-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="df48d-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="df48d-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df48d-121">							objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="df48d-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="df48d-122">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="df48d-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="df48d-p101">Vous pouvez utiliser la propriété **Required** avec la propriété **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** ou **[ValidationRule](field-validationrule-property-dao.md)** pour déterminer la validité du paramètre de la propriété **[Value](field-value-property-dao.md)** de cet objet **Field**. Si la propriété **Required** a la valeur **False**, le champ peut contenir des valeurs **null** ainsi que des valeurs répondant aux conditions spécifiées par les paramètres des propriétés **AllowZeroLength** et **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="df48d-p101">You can use the **Required** property along with the **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to determine the validity of the **[Value](field-value-property-dao.md)** property setting for that **Field** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="df48d-p102">[!REMARQUE] Lorsque vous pouvez définir cette propriété pour un objet **Index** ou un objet **Field**, définissez-la pour l'objet **Field**. En effet, la validité du paramètre de la propriété d'un objet **Field** est vérifiée avant celle d'un objet **Index**.</span><span class="sxs-lookup"><span data-stu-id="df48d-p102">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object. The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="df48d-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="df48d-127">Example</span></span>

<span data-ttu-id="df48d-p103">Cet exemple utilise la propriété **Required** pour signaler les champs de trois tables différentes à renseigner obligatoirement pour ajouter un nouvel enregistrement. La fonction RequiredOutput est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="df48d-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

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
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

