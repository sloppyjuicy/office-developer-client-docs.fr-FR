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
description: Renvoie le caractère ANSI d'un nombre.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418189"
---
# <a name="char-function"></a>Fonction CHAR

Renvoie le caractère ANSI d'un nombre.
  
## <a name="syntax"></a>Syntaxe

CHAR (* * *nombre* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre dont vous souhaitez obtenir le caractère ANSI.  <br/> |
   
## <a name="remarks"></a>Remarques

La chaîne renvoyée comporte un seul caractère. Le paramètre _Number_ doit être un entier compris entre 1 et 255 (inclus), sinon la fonction renvoie une erreur. 
  
## <a name="example"></a>Exemple

CHAR (9) 
  
Renvoie le caractère de tabulation. 
  

