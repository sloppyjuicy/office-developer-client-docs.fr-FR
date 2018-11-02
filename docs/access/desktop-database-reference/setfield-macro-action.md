---
title: SetField, action de macro
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8ca2315a9a84000aa29b88043e4edea05ffb0ea
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922824"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="2b9fe-102">SetField, action de macro</span><span class="sxs-lookup"><span data-stu-id="2b9fe-102">SetField macro action</span></span>


<span data-ttu-id="2b9fe-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b9fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b9fe-104">L'action **DéfinirChamp** peut être utilisée pour assigner une valeur à un champ.</span><span class="sxs-lookup"><span data-stu-id="2b9fe-104">The **SetField** action can be used to assign a value to a field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2b9fe-105">[!REMARQUE] L'action <STRONG>DéfinirChamp</STRONG> est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="2b9fe-105">The <STRONG>SetField</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="2b9fe-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2b9fe-106">Setting</span></span>

<span data-ttu-id="2b9fe-107">L'action **DéfinirChamp** utilise les arguments répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2b9fe-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b9fe-108">Argument</span><span class="sxs-lookup"><span data-stu-id="2b9fe-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="2b9fe-109">Description</span><span class="sxs-lookup"><span data-stu-id="2b9fe-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b9fe-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="2b9fe-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="2b9fe-111">Chaîne qui identifie le champ.</span><span class="sxs-lookup"><span data-stu-id="2b9fe-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b9fe-112"><strong>Valeur</strong></span><span class="sxs-lookup"><span data-stu-id="2b9fe-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="2b9fe-113">Expression qui spécifie la valeur à assigner au champ.</span><span class="sxs-lookup"><span data-stu-id="2b9fe-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2b9fe-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2b9fe-114">Remarks</span></span>

<span data-ttu-id="2b9fe-115">L'action **DéfinirChamp** ne peut pas être utilisée en dehors d'un bloc de données **[CréerEnregistrement](createrecord-data-block.md)** ou **[ModifierEnregistrement](editrecord-data-block.md)**.</span><span class="sxs-lookup"><span data-stu-id="2b9fe-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

