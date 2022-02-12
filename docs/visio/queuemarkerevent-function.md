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
description: Entraîne l’application à tirer un événement marqueur sur votre module, votre code Microsoft Visual Basic pour Applications (VBA) ou votre compl?ment COM.
ms.openlocfilehash: e048a658e36d2370632a950084367f53ae2c8a74
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775300"
---
# <a name="queuemarkerevent-function"></a>Fonction QUEUEMARKEREVENT

Entraîne l’application à tirer un événement marqueur sur votre module, votre code Microsoft Visual Basic pour Applications (VBA) ou votre compl?ment COM. 
  
## <a name="syntax"></a>Syntaxe

QUEUEMARKEREVENT (** *event_string* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Requis  <br/> |**String** <br/> | Chaîne à transmettre à votre handler d’événements. |
   
## <a name="remarks"></a>Remarques

La fonction QUEUEMARKEREVENT fournit aux développeurs un moyen de notifier leur code à partir d’une cellule ShapeSheet et de transmettre des informations spécifiques aux solutions. Lorsque la cellule contenant la formule avec la fonction QUEUEMARKEREVENT est évaluée, l’application déclenche un événement marqueur et transmet  _event_string_ à tous les handlers d’événements qui écoutent l’événement **MarkerEvent** . 
  
Pour plus d’informations sur les événements de marqueur, voir la méthode **QueueMarkerEvent** et les rubriques sur les événements **MarkerEvent** dans la Référence Microsoft Visio Automation. 
  
## <a name="example"></a>Exemple

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Entraîne le déclenchement d’un événement marqueur et transmet la chaîne « MyCustomNotification » aux gestionnaires d’événement qui écoutent l’événement **MarkerEvent**. 
  

