---
title: EST [NOT] NULL (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Détermine si une expression est NULL.
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781829"
---
# <a name="is-not-null-access-custom-web-app"></a>EST [NOT] NULL (accès personnalisé web app)

Détermine si une expression est NULL.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *expression* **Est** [ *Pas* ] **NULL**
  
Le **IS [NOT] NULL** prédicat contient les arguments suivants. 
  
|||
|:-----|:-----|
| *expression*  <br/> |Toute expression valide.  <br/> |
| *NOT*  <br/> |Spécifie que le résultat Boolean être inversée. Le prédicat inverse ses valeurs de retour, retourner la valeur TRUE si la valeur n’est pas NULL et FALSE si la valeur est NULL.  <br/> |
   
## <a name="remarks"></a>Remarques

Si la valeur de *l’expression* est NULL, est NULL renvoie TRUE ; dans le cas contraire, elle renvoie la valeur FALSE. 
  
Si la valeur de l’expression est NULL, n’est pas NULL renvoie la valeur FALSE ; dans le cas contraire, elle renvoie la valeur TRUE.
  

