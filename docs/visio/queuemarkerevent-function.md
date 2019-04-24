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
description: Entraîne le déclenchement d'un événement marqueur pour votre complément, le code Microsoft Visual Basic pour applications (VBA) ou le complément COM.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358725"
---
# <a name="queuemarkerevent-function"></a>Fonction QUEUEMARKEREVENT

Entraîne le déclenchement d'un événement marqueur pour votre complément, le code Microsoft Visual Basic pour applications (VBA) ou le complément COM. 
  
## <a name="syntax"></a>Syntaxe

QUEUEMARKEREVENT (* * *event_string* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Obligatoire  <br/> |**String** <br/> | Chaîne à transmettre à votre gestionnaire d'événements.  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction QUEUEMARKEREVENT fournit aux développeurs un moyen de notifier leur code à partir d’une cellule ShapeSheet et de transmettre des informations spécifiques aux solutions. Lorsque la cellule contenant la formule avec la fonction QUEUEMARKEREVENT est évaluée, l'application déclenche un événement marqueur et transmet _event_string_ à tous les gestionnaires d'événements qui écoutent l'événement **MarkerEvent** . 
  
Pour plus d'informations sur les événements de marque, reportez-vous aux rubriques de la méthode **QueueMarkerEvent** et de l'événement **MarkerEvent** dans la référence d'Automation de Microsoft Visio. 
  
## <a name="example"></a>Exemple

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Entraîne le déclenchement d’un événement marqueur et transmet la chaîne « MyCustomNotification » aux gestionnaires d’événement qui écoutent l’événement **MarkerEvent**. 
  

