---
title: Choose, fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Retourne l’élément à l’index spécifié à partir d’une liste de valeurs.
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781820"
---
# <a name="choose-function-access-custom-web-app"></a>Choose, fonction (accès personnalisé web app)

Retourne l’élément à l’index spécifié à partir d’une liste de valeurs.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**Choisissez** (*Numéro_Index*, *valeur*, [*Value_n*]) 
  
La fonction **Choose** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Numéro_index*  <br/> |Entier qui représente un index à base 1 dans la liste des éléments qui suit.  <br/> |
| *Valeur*  <br/> |Liste des valeurs de tout type de données.  <br/> |
   
## <a name="remarks"></a>Remarques

Si la fourniture *Numéro_Index* n’est pas un entier, la valeur est implicitement convertie en entier. 
  
Si la valeur d’index dépasse les limites du tableau de valeurs, **Choose** renvoie la valeur NULL. 
  

