---
title: HandsOffAfterSave, état
description: Cet article décrit les transitions autorisées de l’état HandsOffAfterSave.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
ms.openlocfilehash: 9afa5d40362eb0ef90660136da2a30d71260fb92
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815197"
---
# <a name="handsoffaftersave-state"></a>HandsOffAfterSave, état

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état HandsOffAfterSave fait partie du processus d’enregistrement du contenu d’un formulaire dans un stockage permanent. Dans cet état, l’objet de formulaire doit s’abstenir d’apporter des modifications aux copies en mémoire des valeurs des propriétés du message, car il peut ne pas y avoir d’autre possibilité d’enregistrer ces modifications. Le tableau suivant décrit les transitions autorisées à partir de l’état HandsOffAfterSave.
  
|**IPersistMessage, méthode**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Ouvrez tous les objets incorporés. Les données du message stocké dans  _pMessage sont garanties_ comme le message dans l’appel [IPersistMessage::Save](ipersistmessage-save.md) précédent. Si l’appel **SaveCompleted** réussit, entrez l’état Normal. Sinon, définissez la dernière erreur sur E_OUTOFMEMORY et restez dans l’état HandsOffAfterSave. |[Normal](normal-state.md) ou HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Définissez la dernière erreur sur E_INVALIDARG ou E_UNEXPECTED. |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save** ou [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Définissez la dernière erreur sur et retournez E_UNEXPECTED. |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Chargez l’objet de formulaire avec les données du message cible. Cet appel peut se produire lorsque l’objet de formulaire passe au message suivant ou précédent dans un dossier. |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retourne la dernière erreur. |HandsOffAfterSave  <br/> |
|Autres [IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) provenant d’autres interfaces  <br/> |Définissez la dernière erreur sur et retournez E_UNEXPECTED. |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

