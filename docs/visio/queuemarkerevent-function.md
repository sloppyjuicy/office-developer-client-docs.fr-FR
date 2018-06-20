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
description: Entraîne le déclenchement d’un événement marqueur vers votre module complémentaire, Microsoft Visual Basic pour Applications (VBA) code, ou un complément COM.
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789380"
---
# <a name="queuemarkerevent-function"></a>QUEUEMARKEREVENT, fonction

Entraîne le déclenchement d’un événement marqueur vers votre module complémentaire, Microsoft Visual Basic pour Applications (VBA) code, ou un complément COM. 
  
## <a name="syntax"></a>Syntaxe

QUEUEMARKEREVENT (** *chaîne_événement* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _chaîne_événement_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | La chaîne à transmettre à votre gestionnaire d’événements.  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction QUEUEMARKEREVENT fournit aux développeurs un moyen de notifier leur code à partir d’une cellule de feuille ShapeSheet et transmettre les informations propres à la solution. Lorsque la cellule contenant la formule avec la fonction QUEUEMARKEREVENT est calculée, l’application déclenche un événement marqueur et transmet _event_string_ à tous les gestionnaires d’événement qui écoutent l’événement **MarkerEvent** . 
  
Pour plus d’informations sur les événements marqueurs, reportez-vous à la méthode **QueueMarkerEvent** et les rubriques d’événement **MarkerEvent** dans la référence Automation de Microsoft Visio. 
  
## <a name="example"></a>Exemple

QUEUEMARKEREVENT ("MyCustomNotification") 
  
Entraîne le déclenchement d’un événement marqueur et transmet la chaîne « MyCustomNotification » aux gestionnaires d’événement qui écoutent l’événement **MarkerEvent** . 
  

