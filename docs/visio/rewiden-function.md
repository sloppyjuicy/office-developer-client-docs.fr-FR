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
ms.openlocfilehash: 4043712e7e520f2640758eae14dab803f0b5a23c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783073"
---
# <a name="rewiden-function"></a>Fonction REWIDEN

Convertit une formule qui produit des codes de caractères 16 bits qui sont élargis de codes de jeu de caractères codés sur un octet ou sur plusieurs octets en une chaîne de codes de caractères Unicode 16 bits, à l’aide des jeux de caractères spécifiés. 
  
## <a name="syntax"></a>Syntaxe

REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Requis  <br/> |**String** <br/> |Jeu de caractères du document source |
| _dstCharSet_ <br/> |Requis  <br/> |**String** <br/> | Jeu de caractères du document de destination |
| _text_ <br/> |Requis  <br/> |**String** <br/> |Texte à convertir |
   
## <a name="remarks"></a>Remarques

La fonction REWIDEN est utilisée pour la conversion automatique de documents Visio 2002 en documents Visio 2003. Une utilisation à une autre fin n’est pas recommandée.
  

