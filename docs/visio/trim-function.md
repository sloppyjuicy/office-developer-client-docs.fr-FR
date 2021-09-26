---
title: TRIM, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
ms.localizationpriority: medium
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Supprime tout l’espace du texte, à l’exception des espaces simples entre les mots.
ms.openlocfilehash: e6d8263585754db88a1500a5fbe20a56ef4fe633
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627260"
---
# <a name="trim-function"></a>Fonction TRIM

Supprime tout l’espace du texte, à l’exception des espaces simples entre les mots. 
  
## <a name="syntax"></a>Syntaxe

TRIM (** *texte* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> |Texte dont vous souhaitez supprimer les espaces.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Vous pouvez utiliser la fonction TRIM sur du texte provenant d’une autre application qui utilise un espacement irrégulier.
  
## <a name="example"></a>Exemple

TRIM (« 1er janvier 2003 « ) 
  
Renvoie "2 janvier 2003". 
  

