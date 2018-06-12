---
title: REWIDEN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Convertit une formule qui produit élargies codes de jeu de caractères codé sur un ou plusieurs octets en une chaîne de codes de caractères Unicode 16 bits, les jeux de caractères spécifié à l’aide de codes de caractères 16 bits.
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789485"
---
# <a name="rewiden-function"></a>REWIDEN, fonction

Convertit une formule qui produit élargies codes de jeu de caractères codé sur un ou plusieurs octets en une chaîne de codes de caractères Unicode 16 bits, les jeux de caractères spécifié à l’aide de codes de caractères 16 bits. 
  
## <a name="syntax"></a>Syntaxe

REWIDEN, (** *srcCharSet* **, ** *dstCharSet* **, ** *texte* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Jeu de caractères du document source  <br/> |
| _dstCharSet_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Jeu de caractères du document de destination  <br/> |
| _text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Texte à convertir  <br/> |
   
## <a name="remarks"></a>Note

La fonction REWIDEN est utilisée pour la conversion automatique de documents Visio 2002 en documents Visio 2003. Une utilisation à une autre fin n’est pas recommandée.
  

