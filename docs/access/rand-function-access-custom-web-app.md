---
title: Rand Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Renvoie un nombre pseudo-aléatoire entre 0 et 1.
ms.openlocfilehash: 9c724166daa094b5310e225cee96a73f787f9ec7
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179668"
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
| *Seed*  <br/> |Expression d’un groupe de valeurs qui donne la valeur de début. Si *Seed* n’est pas spécifié, une valeur d’amorçage est affectée de manière aléatoire.  <br/> |

## <a name="remarks"></a>Remarques

Les appels répétitifs de **la fonction Rand** avec la même amorçage retournent les mêmes résultats.
  