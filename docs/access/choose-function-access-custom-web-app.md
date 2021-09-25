---
title: Choose function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Renvoie l’élément à l’index spécifié à partir d’une liste de valeurs.
ms.openlocfilehash: 3b2ce27b0bd43c2db1d28f90a0ffbd5c2c206496
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573333"
---
# <a name="choose-function-access-custom-web-app"></a>Choose function (Access custom web app)

Renvoie l’élément à l’index spécifié à partir d’une liste de valeurs.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**Choose** (*IndexNumber*, *Value*, [*Value_n*]) 
  
La **fonction Choose** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *IndexNumber*  <br/> |Expression d’un nombre integer qui représente un index de base 1 dans la liste des éléments qui le suivent.  <br/> |
| *Valeur*  <br/> |Liste des valeurs de n’importe quel type de données.  <br/> |
   
## <a name="remarks"></a>Remarques

Si  *IndexNumber fourni n’est*  pas un nombre nombre, la valeur est implicitement convertie en un nombre. 
  
Si la valeur d’index dépasse les limites du tableau de valeurs, **Choose** renvoie la valeur NULL. 
  

