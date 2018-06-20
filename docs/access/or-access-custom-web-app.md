---
title: OU (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combine les deux conditions. Renvoie la valeur TRUE lorsqu’une des deux conditions est remplie.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781953"
---
# <a name="or-access-custom-web-app"></a>OU (accès personnalisé web app)

Combine les deux conditions. Renvoie la valeur TRUE lorsqu’une des deux conditions est remplie.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *BooleanExpression* **Ou** *BooleanExpression* 
  
L’opérateur **Or** utilise l’argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Toute expression valide qui retourne la valeur TRUE ou FALSE.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque plusieurs opérateurs logiques sont utilisés dans une instruction, **ou** les opérateurs sont évalués après les opérateurs **et** . Toutefois, vous pouvez modifier l’ordre d’évaluation à l’aide de parenthèses. 
  
Le tableau suivant montre le résultat de l’opérateur **ou** . 
  
||**LA VALEUR TRUE**|**FALSE**|
|:-----|:-----|:-----|
|**LA VALEUR TRUE** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

