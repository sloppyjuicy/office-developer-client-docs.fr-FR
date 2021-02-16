---
title: DOOLEVERB, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Exécute un verbe pour l’objet OLE.
ms.openlocfilehash: c339d03a00afdf7f777bb0624ddb8fa75f277e05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435661"
---
# <a name="dooleverb-function"></a>Fonction DOOLEVERB

Exécute un verbe pour l’objet OLE.
  
## <a name="syntax"></a>Syntaxe

DOOLEVERB( » ** *verb* ** « ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _« verb »_ <br/> |Obligatoire  <br/> |**String** <br/> |Verbe à exécuter  <br/> |
   
## <a name="remarks"></a>Remarques

Dans les versions précédentes de Visio, cette fonction s’appelait _DOOLEVERB. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre style. 
  
## <a name="example"></a>Exemple

DOOLEVERB(« edit »)
  
Exécute le programme de l’objet OLE et affiche l’objet lié ou imbriqué pour qu’il puisse être modifié.
  

