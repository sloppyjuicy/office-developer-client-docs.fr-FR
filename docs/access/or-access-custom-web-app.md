---
title: OU (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combine deux conditions. Renvoie la valeur TRUE lorsque l'une des deux conditions est true.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308070"
---
# <a name="or-access-custom-web-app"></a>OU (application Web personnalisée Access)

Combine deux conditions. Renvoie la valeur TRUE lorsque l'une des deux conditions est true.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 *BooleanExpression* **Ou** *BooleanExpression* 
  
L'opérateur **or** utilise l'argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Toute expression valide qui renvoie la valeur TRUE ou FALSe.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque plusieurs opérateurs logiques sont utilisés dans une instruction, **ou** les opérateurs sont évalués après **les opérateurs and** . Toutefois, vous pouvez modifier l'ordre d'évaluation en utilisant des parenthèses. 
  
Le tableau suivant montre le résultat de l'opérateur **or** . 
  
||**A**|**TRUE**|
|:-----|:-----|:-----|
|**A** <br/> |TRUE  <br/> |TRUE  <br/> |
|**TRUE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

