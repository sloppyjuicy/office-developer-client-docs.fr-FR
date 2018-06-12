---
title: MSOSHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: f5f6eb0b6009473dcec017e951cca2f90b6c4d55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789157"
---
# <a name="msoshade-function"></a>MSOSHADE, fonction

Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

MSOSHADE (** *couleur* **, ** *- deltaLum* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**RGB** <br/> |Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur.  <br/> |
| _-deltaLum_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Pourcentage de modification vers blanc (-100 %) ou noir (100 %) à partir de la valeur de _couleur_ .  <br/> |
   
## <a name="remarks"></a>Note

Plus la valeur _color_ est blanc ou du noir, moins la modification de l’ombre qui est généré par une valeur spécifique _- deltaLum_ . 
  

