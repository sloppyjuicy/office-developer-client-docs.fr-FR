---
title: État HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 274e7206171e1874e3625896952f861d25f3b382
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564534"
---
# <a name="handsoffaftersave-state"></a>État HandsOffAfterSave

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’état HandsOffAfterSave fait partie du processus de l’enregistrement du contenu d’un formulaire dans un stockage permanent. Dans cet état, l’objet de formulaire doit ne pas apporter des modifications à la copie en mémoire des valeurs des propriétés du message, car il peut ne pas être une autre possibilité d’enregistrer ces modifications. Le tableau suivant décrit les transitions autorisées à partir de l’état HandsOffAfterSave.
  
|**Méthode IPersistMessage**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage ! =_ NULL)  <br/> |Ouvrir des objets incorporés. Les données dans le message stockée dans _pMessage_ sont garanties être la même que le message dans l’appel [IPersistMessage::Save](ipersistmessage-save.md) précédent. Si l’appel de **méthode SaveCompleted** réussit, entrez son état Normal. Dans le cas contraire, la valeur de la dernière erreur E_OUTOFMEMORY et rester à l’état HandsOffAfterSave.  <br/> |[Normal](normal-state.md) ou HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)  <br/> |La valeur la dernière erreur E_INVALIDARG ou E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Enregistrer**ou [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Définissez la dernière erreur à et E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Chargement de l’objet de formulaire avec des données à partir du message cible. Cet appel peut se produire lorsque l’objet de formulaire va le message suivant ou précédent dans un dossier.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoie la dernière erreur.  <br/> |HandsOffAfterSave  <br/> |
|Autres [IPersistMessage : IUnknown](ipersistmessageiunknown.md) méthodes ou autres interfaces  <br/> |Définissez la dernière erreur à et E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

