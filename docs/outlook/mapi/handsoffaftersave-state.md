---
title: État HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406604"
---
# <a name="handsoffaftersave-state"></a>État HandsOffAfterSave

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'État HandsOffAfterSave fait partie du processus d'enregistrement du contenu d'un formulaire dans un emplacement de stockage permanent. Dans cet État, l'objet Form ne doit pas apporter de modifications aux copies en mémoire des propriétés du message, car il se peut qu'il n'y ait pas une autre opportunité d'enregistrer ces modifications. Le tableau suivant décrit les transitions autorisées à partir de l'État HandsOffAfterSave.
  
|**Méthode IPersistMessage**|**Action**|**Nouvel État**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ null)  <br/> |Ouvrez les objets incorporés. Les données contenues dans le message stocké dans _pMessage_ sont garanties de la même manière que le message de l'appel [IPersistMessage:: Save](ipersistmessage-save.md) précédent. Si l'appel **SaveCompleted** réussit, entrez l'état normal. Dans le cas contraire, définissez la dernière erreur sur E_OUTOFMEMORY et restez dans l'État HandsOffAfterSave.  <br/> |[Normal](normal-state.md) ou HandsOffAfterSave  <br/> |
|**IPersistMessage:: SaveCompleted** (_pMessage = =_ null)  <br/> |Définissez la dernière erreur sur E_INVALIDARG ou E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md), **Enregistrer**ou [IPersistMessage:: InitNew](ipersistmessage-initnew.md) <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Charge l'objet Form avec les données du message cible. Cet appel peut se produire lorsque l'objet de formulaire passe au message suivant ou précédent dans un dossier.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur.  <br/> |HandsOffAfterSave  <br/> |
|Autres [IPersistMessage:](ipersistmessageiunknown.md) méthodes ou méthodes IUnknown à partir d'autres interfaces  <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

