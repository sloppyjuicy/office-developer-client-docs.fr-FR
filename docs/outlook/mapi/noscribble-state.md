---
title: État NoScribble
description: L’état NoScribble indique que les modifications apportées à un message sont en cours d’enregistrement. L’enregistrement réel des valeurs se fait lorsque la méthode IPersistMessageSave de l’objet de formulaire est appelée.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
ms.openlocfilehash: dfc8c09607bc1595d6e75c4cb998ad1e9dc5cf96
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852431"
---
# <a name="noscribble-state"></a>État NoScribble

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état NoScribble indique que les modifications apportées à un message sont enregistrées. L’enregistrement réel des valeurs stockées dans l’interface utilisateur de l’objet de formulaire se produit lorsque la méthode [IPersistMessage::Save](ipersistmessage-save.md) de l’objet de formulaire est appelée par l’application cliente. Le tableau suivant décrit les transitions autorisées à partir de l’état NoScribble. 
  
|Méthode IPersistMessage** **|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)  <br/> |Si l’indicateur  _fSameAsLoad_ était TRUE sur l’appel [IPersistMessage::Save](ipersistmessage-save.md) qui a provoqué l’entrée du formulaire dans l’état NoScribble et que le message a été modifié, marquez en interne les modifications comme enregistrées et appelez la méthode [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) . |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)  <br/> |Appelez la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (similaire à la méthode OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) ) suivie des actions **SaveCompleted** normales. Si **SaveCompleted** a réussi, entrez l’état Normal. Sinon, entrez l’état [HandsOffAfterSave](handsoffaftersave-state.md) . |Normal ou HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Appeler de manière **récursive la méthode HandsOffMessage sur les messages incorporés** ou la méthode OLE **IPersistStorage::HandsOffStorage** sur les objets OLE incorporés. Libérez l’objet de message et tous les messages ou objets incorporés. |HandsOffAfterSave  <br/> |
|**Save**, [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur sur et retournez E_UNEXPECTED. |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retourne la dernière erreur. |NoScribble  <br/> |
|Autres [IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) provenant d’autres interfaces  <br/> |Définissez la dernière erreur sur et retournez E_UNEXPECTED. |NoScribble  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

