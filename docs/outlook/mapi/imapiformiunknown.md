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
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321776"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux visionneuses de formulaires de travailler avec les contextes d'affichage de formulaire et les notifications de formulaire, d'exécuter des verbes de formulaire et d'arrêter des formulaires.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Exposé par:  <br/> |Objets de formulaires  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIForm  <br/> |
|Type de pointeur:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Établit un contexte d'affichage pour le formulaire.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Renvoie le contexte d'affichage actuel du formulaire.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Ferme le formulaire.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Demande que le formulaire effectue toutes les tâches associées à un verbe spécifique.  <br/> |
|[Recommander](imapiform-advise.md) <br/> |Inscrit une visionneuse de formulaires pour les notifications relatives aux événements qui affectent le formulaire.  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |Annule une inscription pour les notifications avec une visionneuse de formulaires **** précédemment établie par appel de la méthode Advise.  <br/> |
|[Généré](imapiform-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet Form.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

