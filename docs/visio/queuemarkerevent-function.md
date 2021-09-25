---
title: QUEUEMARKEREVENT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
ms.localizationpriority: medium
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Entraîne le tir d’un événement marqueur par l’application vers votre module, votre code Microsoft Visual Basic pour Applications (VBA) ou votre compl?ment COM.
ms.openlocfilehash: 66b00394897f45ed785e5f537d7bb32b2d2b544a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573655"
---
# <a name="queuemarkerevent-function"></a>Fonction QUEUEMARKEREVENT

Entraîne le tir d’un événement marqueur par l’application vers votre module, votre code Microsoft Visual Basic pour Applications (VBA) ou votre compl?ment COM. 
  
## <a name="syntax"></a>Syntaxe

QUEUEMARKEREVENT (** *event_string* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Obligatoire  <br/> |**String** <br/> | Chaîne à transmettre à votre handler d’événements.  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction QUEUEMARKEREVENT fournit aux développeurs un moyen de notifier leur code à partir d’une cellule ShapeSheet et de transmettre des informations spécifiques aux solutions. Lorsque la cellule contenant la formule avec la fonction QUEUEMARKEREVENT est évaluée, l’application déclenche un événement marqueur et transmet _event_string à_ tous les handlers d’événements qui écoutent l’événement **MarkerEvent.** 
  
Pour plus d’informations sur les événements de marqueur, voir la méthode **QueueMarkerEvent** et les rubriques sur les événements **MarkerEvent** dans la Référence Microsoft Visio Automation. 
  
## <a name="example"></a>Exemple

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Entraîne le déclenchement d’un événement marqueur et transmet la chaîne « MyCustomNotification » aux gestionnaires d’événement qui écoutent l’événement **MarkerEvent**. 
  

