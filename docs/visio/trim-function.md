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
description: Supprime tout l'espace du texte, à l'exception des espaces simples entre les mots.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435718"
---
# <a name="trim-function"></a>Fonction TRIM

Supprime tout l'espace du texte, à l'exception des espaces simples entre les mots. 
  
## <a name="syntax"></a>Syntaxe

TRIM (* * *Text* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> |Texte dont vous souhaitez supprimer les espaces.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Vous pouvez utiliser la fonction TRIM sur du texte provenant d’une autre application qui utilise un espacement irrégulier.
  
## <a name="example"></a>Exemple

TRIM ("janvier 1, 2003") 
  
Renvoie "2 janvier 2003". 
  

