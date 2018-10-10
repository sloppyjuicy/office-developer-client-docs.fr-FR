---
title: FieldEnum (référence de base de données du bureau Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5efcdbd9da4214d7f2b78ffbcfb81fb13265087e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469261"
---
# <a name="fieldenum"></a><span data-ttu-id="ab083-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="ab083-102">FieldEnum</span></span>


<span data-ttu-id="ab083-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab083-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ab083-104">Spécifie les champs spéciaux référencés dans une collection [Fields](record-object-ado.md) d'un objet [Record](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ab083-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

<span data-ttu-id="ab083-105">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="ab083-105">**Remarks**</span></span>

<span data-ttu-id="ab083-p101">Ces constantes représentent un "raccourci" pour accéder aux champs spéciaux associés à un objet **Record**. Extrayez l'objet [Field](field-object-ado.md) depuis la collection **Fields**, puis obtenez son contenu avec la propriété **Value** de l'objet [Field](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ab083-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab083-108">Constant</span><span class="sxs-lookup"><span data-stu-id="ab083-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="ab083-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab083-109">Value</span></span></p></th>
<th><p><span data-ttu-id="ab083-110">Description</span><span class="sxs-lookup"><span data-stu-id="ab083-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab083-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="ab083-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="ab083-112">-1</span><span class="sxs-lookup"><span data-stu-id="ab083-112">-1</span></span></p></td>
<td><p><span data-ttu-id="ab083-113">Référence le champ contenant l’objet <a href="stream-object-ado.md">Stream</a> par défaut associé à un <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab083-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab083-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="ab083-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="ab083-115">-2</span><span class="sxs-lookup"><span data-stu-id="ab083-115">-2</span></span></p></td>
<td><p><span data-ttu-id="ab083-116">Référence le champ contenant la chaîne d’URL absolue du <strong>Record</strong> en cours.</span><span class="sxs-lookup"><span data-stu-id="ab083-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

