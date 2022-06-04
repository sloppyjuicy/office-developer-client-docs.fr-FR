---
title: État non initialisé
description: Décrit la façon dont l’état non initialisé est l’état initial dans lequel les objets de formulaire doivent se trouver lors de leur création initiale.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
ms.openlocfilehash: 6d0e096e0cbfc95ab0760fd7a5da1fe11a2ac7be
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894368"
---
# <a name="uninitialized-state"></a>État non initialisé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état non initialisé est l’état initial dans lequel les objets de formulaire doivent se trouver lors de leur création initiale. Les objets de formulaire sont initialisés avec des données de message lorsqu’une application cliente appelle la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) sur l’objet de formulaire. Le tableau suivant décrit les transitions autorisées à partir de l’état unitialisé. 
  
|**IPersistMessage, méthode**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Chargez l’objet de formulaire avec les données par défaut. |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Chargez l’objet de formulaire avec les données du message cible. |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Renvoyez la réussite ou définissez la dernière erreur sur et renvoyez E_UNEXPECTED. |Non initialisé  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retourne la dernière erreur. |Non initialisé  <br/> |
|Autres [IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) provenant d’autres interfaces  <br/> |Définissez la dernière erreur sur et retournez E_UNEXPECTED. |Non initialisé  <br/> |
   
## <a name="see-also"></a>Voir aussi



[État normal](normal-state.md)
  
[États de formulaire](form-states.md)

