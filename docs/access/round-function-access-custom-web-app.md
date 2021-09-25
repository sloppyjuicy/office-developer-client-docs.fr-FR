---
title: Round Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Renvoie une valeur numérique, arrondie ou tronquée, à la longueur ou à la précision spécifiée.
ms.openlocfilehash: e974cecbc2f602af12ba7aa572541c2f9bee319f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593067"
---
# <a name="round-function-access-custom-web-app"></a>Round Function (Access custom web app)

Renvoie une valeur numérique, arrondie ou tronquée, à la longueur ou à la précision spécifiée.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ]) 
  
La **fonction Round** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Number*  <br/> |Expression numérique.  <br/> |
| *Précision*  <br/> |Précision à laquelle le  *nombre*  doit être arrondi.  *La*  précision doit être une expression numérique. Lorsque  *la*  précision est un nombre positif,  *le*  nombre est arrondi au nombre de positions décimales spécifié par la longueur. Lorsque  *precision*  est un nombre négatif,  *number*  est arrondi à gauche de la virgule décimale, comme spécifié par la longueur.  <br/> |
| *TruncateInsteadOfRound*  <br/> |Type d’opération à effectuer. Lorsqu’il est omis ou qu’il est 0,  *le nombre*  est arrondi. Lorsqu’une valeur autre que 0 est spécifiée,  *number*  est tronqué. La valeur par défaut est 0.  <br/> |
   
## <a name="remarks"></a>Remarques

 **Round** renvoie toujours une valeur. Si la longueur est négative et supérieure au nombre de chiffres avant la virgule, **round** renvoie 0. 
  

