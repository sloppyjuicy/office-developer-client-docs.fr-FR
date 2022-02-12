---
title: MSOSHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: adfb76e2870824a42da061d26097e29b1e6ea994
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788849"
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
| _color_ <br/> |Obligatoire  <br/> |**RGB** <br/> |Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur. |
| _-deltaLum_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Pourcentage de changement en blanc (-100 %) ou noir (100 %) par rapport à la valeur  _de_ couleur. |
   
## <a name="remarks"></a>Remarques

Plus la valeur  _de couleur_ est proche du blanc ou du noir, plus la modification de l’ombre produite par une valeur  _-deltaLum_ spécifique est faible. 
  

