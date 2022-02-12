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
ms.openlocfilehash: a08c1cd45101ff9a5a5ac793623e615602762aad
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782317"
---
# <a name="dooleverb-function"></a>Fonction DOOLEVERB

Exécute un verbe pour l’objet OLE.
  
## <a name="syntax"></a>Syntaxe

DOOLEVERB( » ** *verb* ** « ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _« verb »_ <br/> |Requis  <br/> |**String** <br/> |Verbe à exécuter |
   
## <a name="remarks"></a>Remarques

Dans les versions précédentes de Visio, cette fonction s’appelait _DOOLEVERB. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre style. 
  
## <a name="example"></a>Exemple

DOOLEVERB(« edit »)
  
Exécute le programme de l’objet OLE et affiche l’objet lié ou imbriqué pour qu’il puisse être modifié.
  

