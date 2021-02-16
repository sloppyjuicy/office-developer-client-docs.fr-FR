---
title: THEMEGUARD, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protège les cellules de mise en forme d’une forme pour s’assurer qu’elles utilisent les aspects appropriés du thème actuel.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404945"
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
  

