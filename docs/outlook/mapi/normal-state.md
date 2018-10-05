---
title: État normal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395790"
---
# <a name="normal-state"></a>État normal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état Normal est où l’objet form passe la plupart de ses temps d’attente pour les applications clientes initier une action tels qu’enregistrer les modifications et fermer le formulaire. Le tableau suivant décrit les transitions autorisées à partir de son état Normal.
  
|**Méthode IPersistMessage**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md) (_pMessage ==_ NULL, _fSameAsLoad ==_ TRUE)  <br/> ou -  <br/> **IPersistMessage::Save** (_pMessage ! =_ NULL, _fSameAsLoad ==_ FALSE)  <br/> |Récursive enregistrer tous les objets OLE incorporés qui ont été modifiés. Enregistrer les données de message dans l’objet du message. Stocker l’indicateur _fSameAsLoad_ pour une utilisation ultérieure dans l’état de [NoScribble](noscribble-state.md) .  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save** (_pMessage ! =_ NULL, _fSameAsLoad ==_ TRUE)  <br/> |Ceci est la même que le cas précédent, sauf que cet appel **Enregistrer** est utilisé dans les situations de mémoire insuffisante et ne doit pas échouer par manque de mémoire.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Appel de manière récursive la méthode **HandsOffMessage** sur des messages incorporés ou OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) sur les objets OLE incorporés. Version de l’objet du message et des messages incorporés ni objet.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur à et E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoie la dernière erreur.  <br/> |Normal  <br/> |
|Autres [IPersistMessage : IUnknown](ipersistmessageiunknown.md) méthodes ou autres interfaces  <br/> |Implémenter comme décrit dans la documentation pour les [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface.  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

