---
title: OR (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combine deux conditions. Renvoie TRUE lorsque l’une des deux conditions est vraie.
ms.openlocfilehash: 18fefc4f5e17f86ac4a307256f8a5b3a6887cdbe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631530"
---
# <a name="or-access-custom-web-app"></a>OR (Application web personnalisée Access)

Combine deux conditions. Renvoie TRUE lorsque l’une des deux conditions est vraie.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *BooleanExpression* **ou** *BooleanExpression* 
  
**L’opérateur Or** utilise l’argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Toute expression valide qui renvoie TRUE ou FALSE.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque plusieurs opérateurs logiques sont utilisés dans une instruction, les opérateurs **Or** sont évalués après les opérateurs **And.** Toutefois, vous pouvez modifier l’ordre d’évaluation à l’aide de parenthèses. 
  
Le tableau suivant indique le résultat de **l’opérateur Or.** 
  
||**TRUE**|**FALSE**|
|:-----|:-----|:-----|
|**TRUE** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

