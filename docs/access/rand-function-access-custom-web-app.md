---
title: Rand Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Renvoie un nombre pseudo-aléatoire entre 0 et 1.
ms.openlocfilehash: ef0648fdec7eedd695b8196b6f8f2d652cf9533e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788681"
---
# <a name="rand-function-access-custom-web-app"></a>Rand Function (Access custom web app)

Renvoie un nombre pseudo-aléatoire entre 0 et 1.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="syntax"></a>Syntaxe

 **Rand** ( [  *Seed*  ])
  
La **fonction Rand** contient l’argument suivant.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Seed*  <br/> |Expression d’un groupe de valeurs qui donne la valeur de début. Si *Seed* n’est pas spécifié, une valeur d’amorçage est affectée de manière aléatoire. |

## <a name="remarks"></a>Remarques

Les appels répétitifs de **la fonction Rand** avec la même amorçage retournent les mêmes résultats.
  