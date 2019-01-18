---
title: SkipLine, méthode (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e49b8379f078ad698a4a0040de0eb2e4429fd34
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718776"
---
# <a name="skipline-method-ado"></a><span data-ttu-id="0793d-102">SkipLine, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="0793d-102">SkipLine method (ADO)</span></span>


<span data-ttu-id="0793d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0793d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0793d-104">Saute une ligne complète lors de la lecture d'un flux de texte.</span><span class="sxs-lookup"><span data-stu-id="0793d-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="0793d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0793d-105">Syntax</span></span>

<span data-ttu-id="0793d-106">*Flux de données*. SkipLine</span><span class="sxs-lookup"><span data-stu-id="0793d-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="0793d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0793d-107">Remarks</span></span>

<span data-ttu-id="0793d-p101">Tous les caractères, y compris le séparateur de ligne suivante, sont ignorés. Par défaut, [LineSeparator](lineseparator-property-ado.md) prend la valeur **adCRLF**. Si vous tentez de revenir au-delà de [EOS](eos-property-ado.md), la position actuelle reste simplement au niveau de **EOS**.</span><span class="sxs-lookup"><span data-stu-id="0793d-p101">All characters up to, and including the next line separator, are skipped. By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**. If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="0793d-111">La méthode **SkipLine** est utilisée avec des flux de texte ([Type](type-property-ado-stream.md) prend la valeur **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="0793d-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>

