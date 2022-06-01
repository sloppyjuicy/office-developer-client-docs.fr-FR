---
title: HandsOffFromNormal State
description: Cet article décrit les transitions autorisées de l’état HandsOffFromNormal.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
ms.openlocfilehash: cc152c69b5d62f47a80596b1b077f74ae99284b6
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812389"
---
# <a name="handsofffromnormal-state"></a>HandsOffFromNormal State

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état HandsOffFromNormal est très similaire à l’état [HandsOffAfterSave](handsoffaftersave-state.md) . Il fait partie du processus d’enregistrement du contenu d’un formulaire dans un stockage permanent. Dans cet état, l’objet de formulaire doit s’abstenir d’apporter des modifications aux copies en mémoire des valeurs des propriétés du message, car il peut ne pas y avoir d’autre possibilité d’enregistrer ces modifications. Le tableau suivant décrit les transitions autorisées à partir de l’état HandsOffFromNormal. 
  
|Méthode IPersistMessage** **|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Remplacez le message de l’objet message par  _pMessage_, qui remplace le message révoqué par l’appel précédent à [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md). Les données contenues dans le nouveau message sont garanties comme dans le message révoqué. Le message ne doit pas être marqué comme propre, ni [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) être appelé après cet appel. Si l’appel **SaveCompleted** réussit, entrez l’état [Normal](normal-state.md) . Sinon, restez dans l’état HandsOffFromNormal. |Normal ou HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Définissez la dernière erreur sur E_UNEXPECTED. |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur sur E_UNEXPECTED. |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retourne la dernière erreur. |HandsOffFromNormal  <br/> |
|Autres [IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) provenant d’autres interfaces  <br/> |Définissez la dernière erreur sur E_UNEXPECTED. |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

