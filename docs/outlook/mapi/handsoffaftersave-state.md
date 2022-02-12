---
title: HandsOffAfterSave, état
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ff8c81e80b41b935b265a13ffe3d5d8bf915f60e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62789192"
---
# <a name="handsoffaftersave-state"></a>HandsOffAfterSave, état

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état HandsOffAfterSave fait partie du processus d’enregistrement du contenu d’un formulaire dans un stockage permanent. Dans cet état, l’objet de formulaire doit s’empêcher d’apporter des modifications aux copies en mémoire des valeurs des propriétés du message, car il est possible qu’il n’y a pas d’autre opportunité d’enregistrer ces modifications. Le tableau suivant décrit les transitions autorisées à partir de l’état HandsOffAfterSave.
  
|**Méthode IPersistMessage**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Ouvrez tous les objets incorporés. Les données du message stocké dans  _pMessage sont garanties_ d’être identiques au message de l’appel [IPersistMessage::Save](ipersistmessage-save.md) précédent. Si **l’appel SaveCompleted** réussit, entrez l’état Normal. Sinon, définissez la dernière erreur sur E_OUTOFMEMORY et restez dans l’état HandsOffAfterSave. |[Normal](normal-state.md) ou HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Définissez la dernière erreur sur E_INVALIDARG ou E_UNEXPECTED. |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save** ou [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED. |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Chargez l’objet de formulaire avec les données du message cible. Cet appel peut se produire lorsque l’objet formulaire passe au message suivant ou précédent dans un dossier. |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur. |HandsOffAfterSave  <br/> |
|Autres [méthodes IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) à partir d’autres interfaces  <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED. |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

