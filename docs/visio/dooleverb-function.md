---
title: DOOLEVERB, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
ms.localizationpriority: medium
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Exécute un verbe pour l’objet OLE.
ms.openlocfilehash: 93f69735dbf1d2ae31f0d8c33306c422ecafbfb7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590281"
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
  

