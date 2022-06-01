---
title: IMAPIForm IUnknown
description: IMAPIFormIUnknown permet aux visionneuses de formulaires de travailler avec des contextes d’affichage de formulaires et des notifications de formulaire, d’effectuer des verbes de formulaire et d’arrêter les formulaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
ms.openlocfilehash: 46e8c45adeb0a9048b2c493fd02e5ca0d38939db
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816338"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux visionneuses de formulaires de travailler avec des contextes d’affichage de formulaire et une notification de formulaire, d’effectuer des verbes de formulaire et d’arrêter les formulaires.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets de formulaires  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIForm  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Établit un contexte d’affichage pour le formulaire. |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Retourne le contexte d’affichage actuel du formulaire. |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Ferme le formulaire. |
|[DoVerb](imapiform-doverb.md) <br/> |Demande que le formulaire effectue toutes les tâches associées à un verbe spécifique. |
|[Conseiller](imapiform-advise.md) <br/> |Inscrit une visionneuse de formulaires pour les notifications sur les événements qui affectent le formulaire. |
|[Non-surveillance](imapiform-unadvise.md) <br/> |Annule une inscription pour les notifications avec une visionneuse de formulaires précédemment établie en appelant **Conseiller**. |
|[Getlasterror](imapiform-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite dans l’objet de formulaire. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

