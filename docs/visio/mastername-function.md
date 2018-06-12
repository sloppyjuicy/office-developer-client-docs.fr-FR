---
title: MASTERNAME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Renvoie un nom de feuille maître sous forme de chaîne, ou ne renvoie la chaîne « aucune forme de base » si la feuille ne possède pas une forme de base.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789079"
---
# <a name="mastername-function"></a>MASTERNAME, fonction

Renvoie un nom de feuille maître sous forme de chaîne ou la chaîne «\<aucune forme de base\>» si la feuille ne possède pas une forme de base.
  
## <a name="syntax"></a>Syntaxe

MASTERNAME ([** *Idlang_opt* **]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _Idlang_opt_ <br/> |Facultatif  <br/> |**Number** <br/> |Permet de spécifier une langue pour la chaîne à laquelle la fonction renvoie. Utilisez 0 (valeur par défaut) pour spécifier la langue locale et 750 pour la langue universelle.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

Si vous utilisez un code de langue interdit, la langue locale est utilisée. 
  

