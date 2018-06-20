---
title: THEMEGUARD, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protège les cellules de mise en forme d’une forme afin qu’ils utilisent les aspects appropriés du thème actif.
ms.openlocfilehash: 10a7772995b9cc22e53ff577b2f663d7c97d0816
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789888"
---
# <a name="themeguard-function"></a><span data-ttu-id="39e0f-103">THEMEGUARD, fonction</span><span class="sxs-lookup"><span data-stu-id="39e0f-103">THEMEGUARD Function</span></span>

<span data-ttu-id="39e0f-104">Protège les cellules de mise en forme d’une forme afin qu’ils utilisent les aspects appropriés du thème actif.</span><span class="sxs-lookup"><span data-stu-id="39e0f-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="39e0f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39e0f-105">Syntax</span></span>

<span data-ttu-id="39e0f-106">THEMEGUARD()</span><span class="sxs-lookup"><span data-stu-id="39e0f-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39e0f-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="39e0f-107">Remarks</span></span>

<span data-ttu-id="39e0f-108">Application de la fonction THEMEGUARD à une cellule protège-t-il pas par rapport à la mise en forme manuelle de la même manière que l’application de la protection fonction.</span><span class="sxs-lookup"><span data-stu-id="39e0f-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="39e0f-109">Si vous appliquez la mise en forme à la forme dans l’interface utilisateur ou par programme via Automation, la formule THEMEGUARD est remplacée, sauf si vous incluez la fonction SETATREFEXPR dans la formule pour stocker le manuel de mise en forme de valeur.</span><span class="sxs-lookup"><span data-stu-id="39e0f-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="39e0f-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="39e0f-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="39e0f-111">Spécifie que la forme accepte la couleur Accent 2 du thème actif plutôt que la couleur de remplissage de thème principal.</span><span class="sxs-lookup"><span data-stu-id="39e0f-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

