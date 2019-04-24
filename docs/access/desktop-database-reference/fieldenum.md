---
title: FieldEnum (référence de base de données de bureau Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e42dcfe63194364986e5b235c59b011231307a7c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292593"
---
# <a name="fieldenum"></a><span data-ttu-id="b3fcb-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="b3fcb-102">FieldEnum</span></span>

<span data-ttu-id="b3fcb-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3fcb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3fcb-104">Spécifie les champs spéciaux référencés dans une collection [Fields](record-object-ado.md) d'un objet [Record](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b3fcb-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3fcb-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="b3fcb-105">Remarks</span></span>

<span data-ttu-id="b3fcb-p101">Ces constantes représentent un "raccourci" pour accéder aux champs spéciaux associés à un objet **Record**. Extrayez l’objet [Field](field-object-ado.md) depuis la collection **Fields**, puis obtenez son contenu avec la propriété [Value](value-property-ado.md) de l’objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="b3fcb-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b3fcb-108">Constante</span><span class="sxs-lookup"><span data-stu-id="b3fcb-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="b3fcb-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3fcb-109">Value</span></span></p></th>
<th><p><span data-ttu-id="b3fcb-110">Description</span><span class="sxs-lookup"><span data-stu-id="b3fcb-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3fcb-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="b3fcb-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fcb-112">-1</span><span class="sxs-lookup"><span data-stu-id="b3fcb-112">-1</span></span></p></td>
<td><p><span data-ttu-id="b3fcb-113">Référence le champ contenant l’objet <a href="stream-object-ado.md">Stream</a> par défaut associé à un <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3fcb-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3fcb-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="b3fcb-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="b3fcb-115">-2</span><span class="sxs-lookup"><span data-stu-id="b3fcb-115">-2</span></span></p></td>
<td><p><span data-ttu-id="b3fcb-116">Référence le champ contenant la chaîne d’URL absolue du <strong>Record</strong> en cours.</span><span class="sxs-lookup"><span data-stu-id="b3fcb-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

