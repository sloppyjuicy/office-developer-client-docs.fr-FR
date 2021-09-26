---
title: THEMEGUARD, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protège les cellules de mise en forme d’une forme pour s’assurer qu’elles utilisent les aspects appropriés du thème actuel.
ms.openlocfilehash: e29fdd9c148940e047a7f97a8e6d5b72d685f7cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603346"
---
# <a name="themeguard-function"></a>Fonction THEMEGUARD

Protège les cellules de mise en forme d’une forme pour s’assurer qu’elles utilisent les aspects appropriés du thème actuel.
  
## <a name="syntax"></a>Syntaxe

THEMEGUARD()
  
## <a name="remarks"></a>Remarques

L’application de la fonction THEMEGUARD à une cellule ne permet d’éviter une mise en forme manuelle comme le permet l’application de la fonction GUARD. Si vous appliquez une mise en forme à la forme dans l’interface utilisateur ou par programme, à l’aide de l’automation, la formule THEMEGUARD est overridée, sauf si vous incluez la fonction SETATREFEXPR dans la formule pour stocker la valeur de mise en forme manuelle. 
  
## <a name="example"></a>Exemple

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Spécifie que la forme accepte la couleur Accent 2 du thème actif plutôt que la couleur de remplissage de thème principal.
  

