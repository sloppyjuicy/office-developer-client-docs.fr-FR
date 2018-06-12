---
title: MSOTINT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789186"
---
# <a name="msotint-function"></a>MSOTINT, fonction

Modifie la couleur en augmentant sa luminosité du pourcentage spécifié.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

MSOTINT (** *couleur* **, ** *deltaLum* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**RGB** <br/> |Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur.  <br/> |
| _deltaLum_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Pourcentage de modification vers blanc (-100 %) ou noir (100 %) à partir de la valeur de _couleur_ .  <br/> |
   
## <a name="remarks"></a>Note

Plus la valeur _color_ est blanc ou du noir, moins la modification de la teinte générée par une valeur spécifique _deltaLum_ . 
  

