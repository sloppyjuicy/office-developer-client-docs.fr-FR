---
title: MSOTINT, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: dfe5217d7d41331152032f0829869e8663785372
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404770"
---
# <a name="msotint-function"></a>Fonction MSOTINT

Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010

  
## <a name="syntax"></a>Syntaxe

MSOTINT(***color** _, _ *_deltaLum_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *color* <br/> |Obligatoire  <br/> |**RGB** <br/> |Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur. |
| *deltaLum* <br/> |Obligatoire  <br/> |**Entier** <br/> |Pourcentage de changement en blanc (-100 %) ou noir (100 %) par rapport à la valeur  *de* couleur. |

## <a name="remarks"></a>Remarques

Plus la valeur *de couleur* est proche du blanc ou du noir, plus la modification de la teinte produite par une valeur *deltaLum* spécifique est faible.
  