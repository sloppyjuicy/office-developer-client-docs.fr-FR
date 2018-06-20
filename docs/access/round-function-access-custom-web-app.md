---
title: Round, fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Renvoie une valeur numérique, arrondi soit tronqué, à la longueur spécifiée ou la précision.
ms.openlocfilehash: 5a3df4a4ddd7aace5edf886db5988704e5dd6af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781981"
---
# <a name="round-function-access-custom-web-app"></a>Round, fonction (accès personnalisé web app)

Renvoie une valeur numérique, arrondi soit tronqué, à la longueur spécifiée ou la précision.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Arrondir** (*Nombre*, *précision* , [ *TruncateInsteadOfRound* ]) 
  
La fonction **arrondi** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Number*  <br/> |Une expression numérique.  <br/> |
| *Précision*  <br/> |Précision à laquelle le *nombre* est arrondi.  *Précision* doit être une expression numérique. Lorsque la *précision* est un nombre positif, le *nombre* est arrondi au nombre de positions décimales spécifié par longueur. Si un nombre négatif la *précision* , le *nombre* est arrondi à gauche du séparateur décimal, comme spécifié par la longueur.  <br/> |
| *TruncateInsteadOfRound*  <br/> |Le type d’opération à effectuer. Lorsque omis ou a la valeur 0, le *nombre* est arrondi. Lorsqu’une valeur autre que 0 est spécifiée, le *nombre* est arrondi. La valeur par défaut est 0.  <br/> |
   
## <a name="remarks"></a>Remarques

 **Round** renvoie toujours une valeur. Si length est supérieure au nombre de chiffres avant la virgule décimale et négatifs, **Round** renvoie 0. 
  

