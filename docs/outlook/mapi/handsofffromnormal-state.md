---
title: HandsOffFromNormal State
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 45374bfbead9f8f94967149c1f418cf77aa9ebd3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561725"
---
# <a name="handsofffromnormal-state"></a>HandsOffFromNormal State

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état HandsOffFromNormal est très similaire à [l’état HandsOffAfterSave.](handsoffaftersave-state.md) Il fait partie du processus d’enregistrement du contenu d’un formulaire dans un stockage permanent. Dans cet état, l’objet de formulaire doit s’empêcher d’apporter des modifications aux copies en mémoire des valeurs des propriétés du message, car il est possible qu’il n’y a pas d’autre opportunité d’enregistrer ces modifications. Le tableau suivant décrit les transitions autorisées à partir de l’état HandsOffFromNormal. 
  
|Méthode IPersistMessage** **|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Remplacez le message de l’objet de message par  _pMessage,_ qui remplace le message révoqué par l’appel précédent à [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md). Les données du nouveau message sont garanties d’être identiques à dans le message révoqué. Le message ne doit pas être marqué comme propre, et [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) ne doit pas être appelé après cet appel. Si **l’appel SaveCompleted** réussit, entrez [l’état Normal.](normal-state.md) Dans le cas contraire, restez dans l’état HandsOffFromNormal.  <br/> |Normal ou HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Définissez la dernière erreur sur E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur sur E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur.  <br/> |HandsOffFromNormal  <br/> |
|Autres [méthodes IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) à partir d’autres interfaces  <br/> |Définissez la dernière erreur sur E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

