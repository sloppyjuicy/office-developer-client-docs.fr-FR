---
title: MSOSHADE, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: d76ed4b14c312cb0db2628ed436bf5b7bfdacf48
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404480"
---
# <a name="msoshade-function"></a>Fonction MSOSHADE

Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010

  
## <a name="syntax"></a>Syntaxe

MS CRYPTODE(***color**_, _*_-deltaLum_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *color* <br/> |Obligatoire  <br/> |**RGB** <br/> |Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur. |
| *-deltaLum* <br/> |Obligatoire  <br/> |**Entier** <br/> |Pourcentage de modification vers blanc (-100 %) ou noir (100 %) à partir de la valeur *color*. |

## <a name="remarks"></a>Remarques

Plus la valeur *color* est proche du blanc ou du noir, moins la modification de l’ombre générée par une valeur *-deltaLum* spécifique est importante.
  