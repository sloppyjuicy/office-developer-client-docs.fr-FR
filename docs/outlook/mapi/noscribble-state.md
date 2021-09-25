---
title: NoScribble State
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ab70ef11a68b601729138e2ae92adc37cc89266c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592010"
---
# <a name="noscribble-state"></a>NoScribble State

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état NoScribble indique que les modifications apportées à un message sont enregistrées. L’enregistrement réel des valeurs stockées dans l’interface utilisateur de l’objet formulaire se produit lorsque la méthode [IPersistMessage::Save](ipersistmessage-save.md) de l’objet formulaire est appelée par l’application cliente. Le tableau suivant décrit les transitions autorisées à partir de l’état NoScribble. 
  
|Méthode IPersistMessage** **|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)  <br/> |Si l’indicateur _fSameAsLoad_ était TRUE sur l’appel [IPersistMessage::Save](ipersistmessage-save.md) qui a entraîné l’entrée du formulaire dans l’état NoScribble et que le message a été modifié, marquez en interne les modifications comme enregistrées et appelez la méthode [IMAPIViewAdviseSink::OnSaved.](imapiviewadvisesink-onsaved.md)  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)  <br/> |Appelez la méthode [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (similaire à la méthode OLE [IPersistStorage::HandsOffStorage)](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) suivie des actions **Normales SaveCompleted.** Si **SaveCompleted a** réussi, entrez l’état Normal. Dans le cas contraire, entrez [l’état HandsOffAfterSave.](handsoffaftersave-state.md)  <br/> |Normal ou HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Appeler de manière **récursive la méthode HandsOffMessage** sur les messages incorporés ou la méthode OLE **IPersistStorage::HandsOffStorage** sur des objets OLE incorporés. Relâchez l’objet message et tous les messages ou objets incorporés.  <br/> |HandsOffAfterSave  <br/> |
|**Save**, [IPersistMessage::InitNew](ipersistmessage-initnew.md)ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur.  <br/> |NoScribble  <br/> |
|Autres [méthodes IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) à partir d’autres interfaces  <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

