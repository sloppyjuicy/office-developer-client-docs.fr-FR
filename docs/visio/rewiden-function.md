---
title: REWIDEN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
ms.localizationpriority: medium
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Convertit une formule qui produit des codes de caractères 16 bits qui sont élargis de codes de jeu de caractères codés sur un octet ou sur plusieurs octets en une chaîne de codes de caractères Unicode 16 bits, à l’aide des jeux de caractères spécifiés.
ms.openlocfilehash: 35dc1f379c2fd0efc68f31ea92891d2b7914f3b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627631"
---
# <a name="rewiden-function"></a>Fonction REWIDEN

Convertit une formule qui produit des codes de caractères 16 bits qui sont élargis de codes de jeu de caractères codés sur un octet ou sur plusieurs octets en une chaîne de codes de caractères Unicode 16 bits, à l’aide des jeux de caractères spécifiés. 
  
## <a name="syntax"></a>Syntaxe

REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Obligatoire  <br/> |**String** <br/> |Jeu de caractères du document source  <br/> |
| _dstCharSet_ <br/> |Obligatoire  <br/> |**String** <br/> | Jeu de caractères du document de destination  <br/> |
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> |Texte à convertir  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction REWIDEN est utilisée pour la conversion automatique de documents Visio 2002 en documents Visio 2003. Une utilisation à une autre fin n’est pas recommandée.
  

