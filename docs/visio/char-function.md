---
title: CHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Renvoie le caractère ANSI pour un nombre.
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788233"
---
# <a name="char-function"></a>CHAR, fonction

Renvoie le caractère ANSI pour un nombre.
  
## <a name="syntax"></a>Syntaxe

CHAR (** *numéro* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre dont vous souhaitez obtenir le caractère ANSI.  <br/> |
   
## <a name="remarks"></a>Remarques

La chaîne obtenue est un caractère. Le paramètre _nombre_ doit être un entier compris entre 1 et 255 (inclus), ou la fonction renvoie une erreur. 
  
## <a name="example"></a>Exemple

CHAR(9) 
  
Renvoie le caractère de tabulation. 
  

