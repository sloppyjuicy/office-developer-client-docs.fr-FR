---
title: État NoScribble
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 119d162b50048e69168aa864e5d19ad806758456
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575993"
---
# <a name="noscribble-state"></a>État NoScribble

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’état NoScribble indique que les modifications apportées à un message sont enregistrées. L’enregistrement réel des valeurs stockées dans l’interface utilisateur de l’objet de formulaire se produit lorsque la méthode [IPersistMessage::Save](ipersistmessage-save.md) de l’objet form est appelée par l’application cliente. Le tableau suivant décrit les transitions autorisées à partir de l’état NoScribble. 
  
|Méthode IPersistMessage ** **|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage ==_ NULL)  <br/> |Si l’indicateur _fSameAsLoad_ a la valeur TRUE sur l’appel de [IPersistMessage::Save](ipersistmessage-save.md) qui a provoqué l’écran pour entrer l’état de NoScribble et le message a été modifié, en interne marquer les modifications enregistrées et appelez [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) méthode.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ! =_ NULL)  <br/> |Appelez la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (similaire à la méthode OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) ), suivie par les actions de **méthode SaveCompleted** normales. Si la **méthode SaveCompleted** a réussi, entrez son état Normal. Sinon, entrez l’état [HandsOffAfterSave](handsoffaftersave-state.md) .  <br/> |Normal ou HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Appel de manière récursive la méthode **HandsOffMessage** sur des messages incorporés ou OLE **IPersistStorage::HandsOffStorage** sur les objets OLE incorporés. Version de l’objet du message et des messages incorporés ni objet.  <br/> |HandsOffAfterSave  <br/> |
|**Enregistrer**, [IPersistMessage::InitNew](ipersistmessage-initnew.md)ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur à et E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoie la dernière erreur.  <br/> |NoScribble  <br/> |
|Autres [IPersistMessage : IUnknown](ipersistmessageiunknown.md) méthodes ou autres interfaces  <br/> |Définissez la dernière erreur à et E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

