---
title: THEMEGUARD, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protège les cellules de mise en forme d'une forme pour s'assurer qu'elles utilisent les aspects appropriés du thème actuel.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326753"
---
# <a name="themeguard-function"></a><span data-ttu-id="8bdde-103">Fonction THEMEGUARD</span><span class="sxs-lookup"><span data-stu-id="8bdde-103">THEMEGUARD Function</span></span>

<span data-ttu-id="8bdde-104">Protège les cellules de mise en forme d'une forme pour s'assurer qu'elles utilisent les aspects appropriés du thème actuel.</span><span class="sxs-lookup"><span data-stu-id="8bdde-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8bdde-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bdde-105">Syntax</span></span>

<span data-ttu-id="8bdde-106">THEMEGUARD ()</span><span class="sxs-lookup"><span data-stu-id="8bdde-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8bdde-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="8bdde-107">Remarks</span></span>

<span data-ttu-id="8bdde-108">L’application de la fonction THEMEGUARD à une cellule ne permet d’éviter une mise en forme manuelle comme le permet l’application de la fonction GUARD.</span><span class="sxs-lookup"><span data-stu-id="8bdde-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="8bdde-109">Si vous appliquez la mise en forme à la forme dans l'interface utilisateur ou par programme, par le biais de l'automatisation, la formule THEMEGUARD est substituée, sauf si vous incluez la fonction SETATREFEXPR dans la formule pour stocker la valeur de mise en forme manuelle.</span><span class="sxs-lookup"><span data-stu-id="8bdde-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8bdde-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="8bdde-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="8bdde-111">Spécifie que la forme accepte la couleur Accent 2 du thème actif plutôt que la couleur de remplissage de thème principal.</span><span class="sxs-lookup"><span data-stu-id="8bdde-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

