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
ms.openlocfilehash: a18ed56bba5b1441f6ccaaefa45e74f9cc3cc033
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62769973"
---
# <a name="trim-function"></a>Fonction TRIM

Supprime tout l’espace du texte, à l’exception des espaces simples entre les mots. 
  
## <a name="syntax"></a>Syntaxe

TRIM (** *texte* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Requis  <br/> |**String** <br/> |Texte dont vous souhaitez supprimer les espaces. |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Vous pouvez utiliser la fonction TRIM sur du texte provenant d’une autre application qui utilise un espacement irrégulier.
  
## <a name="example"></a>Exemple

TRIM (« 1er janvier 2003 « ) 
  
Renvoie "2 janvier 2003". 
  

