---
title: MSOSHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: 76ba30f977b9a08916ba158f474f57dbf2d9a7a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563041"
---
# <a name="msoshade-function"></a>Fonction MSOSHADE

Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

MS CRYPTODE(** *color* **, ** *-deltaLum* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**RGB** <br/> |Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur.  <br/> |
| _-deltaLum_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Pourcentage de changement vers le blanc (-100 %) ou le noir (100 %) par rapport à la valeur  _de_ couleur.  <br/> |
   
## <a name="remarks"></a>Remarques

Plus la valeur  _de couleur_ est proche du blanc ou du noir, plus la modification de l’ombre produite par une valeur  _-deltaLum_ spécifique est faible. 
  

