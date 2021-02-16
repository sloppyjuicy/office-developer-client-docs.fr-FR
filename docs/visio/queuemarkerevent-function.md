---
title: QUEUEMARKEREVENT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Entraîne l’application à tirer un événement marqueur sur votre module Visual Basic pour Applications code Microsoft (VBA) ou votre compl?ment COM.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418805"
---
# <a name="queuemarkerevent-function"></a>Fonction QUEUEMARKEREVENT

Entraîne l’application à tirer un événement marqueur sur votre module Visual Basic pour Applications code Microsoft (VBA) ou votre compl?ment COM. 
  
## <a name="syntax"></a>Syntaxe

QUEUEMARKEREVENT (** *event_string* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Obligatoire  <br/> |**String** <br/> | Chaîne à transmettre à votre handler d’événements.  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction QUEUEMARKEREVENT fournit aux développeurs un moyen de notifier leur code à partir d’une cellule ShapeSheet et de transmettre des informations spécifiques aux solutions. Lorsque la cellule contenant la formule avec la fonction QUEUEMARKEREVENT est évaluée, l’application déclenche un événement marqueur et transmet _event_string_ à tous les handlers d’événements qui écoutent l’événement **MarkerEvent.** 
  
Pour plus d’informations sur les événements de marqueur, voir la méthode **QueueMarkerEvent** et les rubriques sur les événements **MarkerEvent** dans la Référence Microsoft Visio Automation. 
  
## <a name="example"></a>Exemple

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Entraîne le déclenchement d’un événement marqueur et transmet la chaîne « MyCustomNotification » aux gestionnaires d’événement qui écoutent l’événement **MarkerEvent**. 
  

