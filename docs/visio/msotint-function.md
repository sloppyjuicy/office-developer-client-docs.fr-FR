---
title: MSOTINT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: c3dbb6be736663a615539825bcd3af07accc3d12
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772815"
---
# <a name="msotint-function"></a>Fonction MSOTINT

Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

MSOTINT(** *color* **, ** *deltaLum* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**RGB** <br/> |Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur. |
| _deltaLum_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Pourcentage de changement en blanc (-100 %) ou noir (100 %) par rapport à la valeur  _de_ couleur. |
   
## <a name="remarks"></a>Remarques

Plus la valeur  _de couleur_ est proche du blanc ou du noir, plus la modification de la teinte produite par une valeur  _deltaLum_ spécifique est faible. 
  

