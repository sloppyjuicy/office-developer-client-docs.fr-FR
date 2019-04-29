---
title: État HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426470"
---
# <a name="handsofffromnormal-state"></a>État HandsOffFromNormal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'État HandsOffFromNormal est très semblable à l'état [HandsOffAfterSave](handsoffaftersave-state.md) . Il fait partie du processus d'enregistrement du contenu d'un formulaire dans un emplacement de stockage permanent. Dans cet État, l'objet Form ne doit pas apporter de modifications aux copies en mémoire des propriétés du message, car il se peut qu'il n'y ait pas une autre opportunité d'enregistrer ces modifications. Le tableau suivant décrit les transitions autorisées à partir de l'État HandsOffFromNormal. 
  
|IPersistMessage * * méthode * *|**Action**|**Nouvel État**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ null)  <br/> |Remplacez le message de l'objet message par _pMessage_, qui remplace le message révoqué par l'appel précédent à [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md). Il est garanti que les données du nouveau message sont les mêmes que dans le message révoqué. Le message ne doit pas être marqué comme Clean et [IMAPIViewAdviseSink:: OnSaved](imapiviewadvisesink-onsaved.md) être appelé après cet appel. Si l'appel **SaveCompleted** réussit, entrez l'état [normal](normal-state.md) . Sinon, restez dans l'État HandsOffFromNormal.  <br/> |Normal ou HandsOffFromNormal  <br/> |
|**IPersistMessage:: SaveCompleted** (_pMessage = =_ null)  <br/> |Définissez la dernière erreur sur E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage:: Save](ipersistmessage-save.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md)ou [IPersistMessage:: Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur sur E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur.  <br/> |HandsOffFromNormal  <br/> |
|Autres [IPersistMessage:](ipersistmessageiunknown.md) méthodes ou méthodes IUnknown à partir d'autres interfaces  <br/> |Définissez la dernière erreur sur E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

