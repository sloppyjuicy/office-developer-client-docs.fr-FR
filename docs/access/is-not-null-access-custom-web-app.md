---
title: IS [NOT] NULL (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Détermine si une expression spécifiée est NULL.
ms.localizationpriority: high
ms.openlocfilehash: 7447540d1f7c9769d4192931c62fc53ca5b377f4
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179962"
---
# <a name="is-not-null-access-custom-web-app"></a>IS [NOT] NULL (application web personnalisée Access)

Détermine si une expression spécifiée est NULL.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="syntax"></a>Syntaxe

 *expression* **IS** [  *NOT*  ] **NULL**
  
Le prédicat **IS [NOT] NULL** contient les arguments suivants.
  
|||
|:-----|:-----|
| *expression*  <br/> |Toute expression valide.  <br/> |
| *NOT*  <br/> |Spécifie que le résultat booléen doit être negatif. Le prédicat inverse ses valeurs de retour, en retournant TRUE si la valeur n’est pas NULL et FALSE si la valeur est NULL.  <br/> |
   
## <a name="remarks"></a>Remarques

Si la valeur de l’*expression* est NULL, IS NULL renvoie TRUE ; dans le cas contraire, elle renvoie FALSE.
  
Si la valeur de l’expression est NULL, IS NOT NULL renvoie FALSE ; dans le cas contraire, elle renvoie TRUE.
  