---
title: TRIM, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Supprime tout espace du texte, à l’exception des espaces entre les mots.
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789942"
---
# <a name="trim-function"></a>TRIM, fonction

Supprime tout espace du texte, à l’exception des espaces entre les mots. 
  
## <a name="syntax"></a>Syntaxe

TRIM (** *texte* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Texte dont vous souhaitez supprimer les espaces.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

Vous pouvez utiliser la fonction TRIM sur du texte provenant d’une autre application qui utilise un espacement irrégulier.
  
## <a name="example"></a>Exemple

TRIM (« janvier 1, 2003 ») 
  
Renvoie "2 janvier 2003". 
  

