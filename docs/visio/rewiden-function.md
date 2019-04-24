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
description: ConVertit une formule produisant des codes de caractères 16 bits qui sont des codes de jeu de caractères codés sur un octet ou sur plusieurs octets élargis en une chaîne de codes de caractères Unicode 16 bits, à l'aide des jeux de caractères spécifiés.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326767"
---
# <a name="rewiden-function"></a>Fonction REWIDEN

ConVertit une formule produisant des codes de caractères 16 bits qui sont des codes de jeu de caractères codés sur un octet ou sur plusieurs octets élargis en une chaîne de codes de caractères Unicode 16 bits, à l'aide des jeux de caractères spécifiés. 
  
## <a name="syntax"></a>Syntaxe

ReLARGESn (* * *srcCharSet* * *, * * *dstCharSet* * *, * * *Text* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Obligatoire  <br/> |**String** <br/> |Jeu de caractères du document source  <br/> |
| _dstCharSet_ <br/> |Obligatoire  <br/> |**String** <br/> | Jeu de caractères du document de destination  <br/> |
| _text_ <br/> |Obligatoire  <br/> |**String** <br/> |Texte à convertir  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction REWIDEN est utilisée pour la conversion automatique de documents Visio 2002 en documents Visio 2003. Une utilisation à une autre fin n’est pas recommandée.
  

