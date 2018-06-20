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
# <a name="themeguard-function"></a>THEMEGUARD, fonction

Protège les cellules de mise en forme d’une forme afin qu’ils utilisent les aspects appropriés du thème actif.
  
## <a name="syntax"></a>Syntaxe

THEMEGUARD()
  
## <a name="remarks"></a>Remarques

Application de la fonction THEMEGUARD à une cellule protège-t-il pas par rapport à la mise en forme manuelle de la même manière que l’application de la protection fonction. Si vous appliquez la mise en forme à la forme dans l’interface utilisateur ou par programme via Automation, la formule THEMEGUARD est remplacée, sauf si vous incluez la fonction SETATREFEXPR dans la formule pour stocker le manuel de mise en forme de valeur. 
  
## <a name="example"></a>Exemple

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Spécifie que la forme accepte la couleur Accent 2 du thème actif plutôt que la couleur de remplissage de thème principal.
  

