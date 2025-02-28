---
title: Choose function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Renvoie l’élément à l’index spécifié à partir d’une liste de valeurs.
ms.openlocfilehash: f2a69844a9867044b20a7e971f74dd9cf34fdd26
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777886"
---
# <a name="choose-function-access-custom-web-app"></a>Choose function (Access custom web app)

Renvoie l’élément à l’index spécifié à partir d’une liste de valeurs.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="syntax"></a>Syntaxe

**Choose** (*IndexNumber*, *Value*, [*Value_n*])
  
La **fonction Choose** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *IndexNumber*  <br/> |Expression d’un nombre integer qui représente un index de base 1 dans la liste des éléments qui le suivent. |
| *Valeur*  <br/> |Liste des valeurs de n’importe quel type de données. |

## <a name="remarks"></a>Remarques

Si *indexnumber fourni n’est* pas un nombre integer, la valeur est implicitement convertie en un nombre.
  
Si la valeur d’index dépasse les limites du tableau de valeurs, **Choose** renvoie la valeur NULL.
  