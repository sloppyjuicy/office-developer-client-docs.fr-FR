---
title: SetField, action de macro
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66dfe95aaa335e14b0148d2fcd610abc30556e3a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997496"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="a9f9e-102">SetField, action de macro</span><span class="sxs-lookup"><span data-stu-id="a9f9e-102">SetField macro action</span></span>

<span data-ttu-id="a9f9e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9f9e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9f9e-104">L'action **DéfinirChamp** peut être utilisée pour assigner une valeur à un champ.</span><span class="sxs-lookup"><span data-stu-id="a9f9e-104">The **SetField** action can be used to assign a value to a field.</span></span>

> [!NOTE]
> <span data-ttu-id="a9f9e-105">[!REMARQUE] L'action **DéfinirChamp** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="a9f9e-105">The **SetField** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="a9f9e-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a9f9e-106">Setting</span></span>

<span data-ttu-id="a9f9e-107">L'action **DéfinirChamp** utilise les arguments répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a9f9e-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9f9e-108">Argument</span><span class="sxs-lookup"><span data-stu-id="a9f9e-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="a9f9e-109">Description</span><span class="sxs-lookup"><span data-stu-id="a9f9e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9f9e-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="a9f9e-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a9f9e-111">Chaîne qui identifie le champ.</span><span class="sxs-lookup"><span data-stu-id="a9f9e-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f9e-112"><strong>Valeur</strong></span><span class="sxs-lookup"><span data-stu-id="a9f9e-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="a9f9e-113">Expression qui spécifie la valeur à assigner au champ.</span><span class="sxs-lookup"><span data-stu-id="a9f9e-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a9f9e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a9f9e-114">Remarks</span></span>

<span data-ttu-id="a9f9e-115">L'action **DéfinirChamp** ne peut pas être utilisée en dehors d'un bloc de données **[CréerEnregistrement](createrecord-data-block.md)** ou **[ModifierEnregistrement](editrecord-data-block.md)**.</span><span class="sxs-lookup"><span data-stu-id="a9f9e-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

