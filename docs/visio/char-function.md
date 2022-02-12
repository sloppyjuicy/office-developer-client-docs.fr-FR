---
title: CHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
ms.localizationpriority: medium
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Renvoie le caractère ANSI d’un nombre.
ms.openlocfilehash: 75af7d3ca92a174c9dd8629bb755f4a6e88cfeee
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787442"
---
# <a name="char-function"></a>Fonction CHAR

Renvoie le caractère ANSI d’un nombre.
  
## <a name="syntax"></a>Syntaxe

CHAR(** *number* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Number** <br/> |Nombre dont vous souhaitez obtenir le caractère ANSI. |
   
## <a name="remarks"></a>Remarques

La chaîne renvoyée comporte un seul caractère. Le  _paramètre_ number doit être un nombre compris entre 1 et 255 (inclus), sinon la fonction renvoie une erreur. 
  
## <a name="example"></a>Exemple

CHAR(9) 
  
Renvoie le caractère de tabulation. 
  

