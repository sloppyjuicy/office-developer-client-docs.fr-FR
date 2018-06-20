---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fce8bc45d5cc87c238288653ab989b62076ad451
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783799"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**S’applique à**: Outlook 
  
Permet de visionneuses de formulaire travailler avec des contextes d’affichage de formulaire et les notifications de formulaire, effectuer des verbes formulaire et arrêt de formulaires.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Objets de formulaire  <br/> |
|Implémentée par :  <br/> |Serveurs de formulaire  <br/> |
|Appelée par :  <br/> |Visionneuses de formulaire  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIForm  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Établissement d’un contexte de vue pour le formulaire.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Renvoie le contexte actuel de la vue pour le formulaire.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Ferme le formulaire.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Exige que le formulaire exécute ce que les tâches associe un verbe spécifique.  <br/> |
|[Conseiller](imapiform-advise.md) <br/> |Enregistre une visionneuse de formulaire pour les notifications concernant les événements qui affectent le formulaire.  <br/> |
|[L’avertissement](imapiform-unadvise.md) <br/> |Annule une inscription pour les notifications avec une visionneuse de formulaire précédemment établie via un appel **Advise**.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente se produisant à l’objet form.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

