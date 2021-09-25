---
title: IMAPIForm IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f58ad771c166675ca43d928b9135941a41518976
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551295"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux visionneuses de formulaires de fonctionner avec des contextes d’affichage de formulaire et des notifications de formulaire, d’exécuter des verbes de formulaire et d’arrêter des formulaires.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets de formulaires  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIForm  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Établit un contexte d’affichage pour le formulaire.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Renvoie le contexte d’affichage actuel du formulaire.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Ferme le formulaire.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Demande au formulaire d’effectuer les tâches qu’il associe à un verbe spécifique.  <br/> |
|[Conseiller](imapiform-advise.md) <br/> |Inscrit une visionneuse de formulaires pour les notifications sur les événements qui affectent le formulaire.  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |Annule une inscription pour les notifications auprès d’une visionneuse de formulaires précédemment établie en appelant **Advise**.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

