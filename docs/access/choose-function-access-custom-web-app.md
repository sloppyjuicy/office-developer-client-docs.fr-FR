---
title: Choose, fonction (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Renvoie l'élément situé à l'index spécifié à partir d'une liste de valeurs.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282284"
---
# <a name="choose-function-access-custom-web-app"></a>Choose, fonction (application Web personnalisée Access)

Renvoie l'élément situé à l'index spécifié à partir d'une liste de valeurs.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**Sélectionnez** (*IndexNumber*, *value*, [*Value_n*]) 
  
La **** fonction Choose contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *IndexNumber*  <br/> |Expression de type Integer qui représente un index de base 1 dans la liste des éléments qui le suivent.  <br/> |
| *Valeur*  <br/> |Liste de valeurs de n'importe quel type de données.  <br/> |
   
## <a name="remarks"></a>Remarques

Si le *IndexNumber* fourni n'est pas un entier, la valeur est implicitement convertie en entier. 
  
Si la valeur d'index dépasse les limites du tableau de valeurs, **Choose** renvoie une valeur null. 
  

