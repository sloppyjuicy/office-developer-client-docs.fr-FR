---
title: Fonction exp (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Renvoie la valeur exponentielle de l'expression spécifiée.
ms.openlocfilehash: 30777c41005dfcf1caad896e9e60f0bcfd9d4361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436411"
---
# <a name="exp-function-access-custom-web-app"></a>Fonction exp (application Web personnalisée Access)

Renvoie la valeur exponentielle de l'expression spécifiée.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Exp** (*NumericExpression*) 
  
La fonction **exp** contient l'argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Expression de type double ou d'un type pouvant être converti implicitement en double.  <br/> |
   
## <a name="remarks"></a>Remarques

La constante **e** (2,718281...) est la base des logarithmes naturels. 
  
L'exposant d'un nombre est la constante **e** élevée à la puissance du nombre. Par exemple **exp** (1,0) = e ^ 1.0 = 2.71828182845905 et **exp** (10) = e ^ 10 = 22026.4657948067. 
  
La valeur exponentielle du logarithme népérien d'un nombre est le nombre lui-même: **exp** (log (n)) = n. Et le logarithme népérien de l'exponentiel d'un nombre est le numéro lui-même: LOG (**exp** (n)) = n. 
  

