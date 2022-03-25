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
ms.openlocfilehash: c4a6c65ee60a3ec3d74dc94848f111a7c1605814
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63723283"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux visionneuses de formulaires de fonctionner avec des contextes d’affichage de formulaire et des notifications de formulaire, d’exécuter des verbes de formulaire et d’arrêter des formulaires.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets de formulaires  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIForm  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Établit un contexte d’affichage pour le formulaire. |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Renvoie le contexte d’affichage actuel du formulaire. |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Ferme le formulaire. |
|[DoVerb](imapiform-doverb.md) <br/> |Demande au formulaire d’effectuer toutes les tâches qu’il associe à un verbe spécifique. |
|[Conseiller](imapiform-advise.md) <br/> |Inscrit une visionneuse de formulaires pour les notifications sur les événements qui affectent le formulaire. |
|[Unadvise](imapiform-unadvise.md) <br/> |Annule l’inscription des notifications auprès d’une visionneuse de formulaires précédemment établie en appelant **Advise**. |
|[GetLastError](imapiform-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de formulaire. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

