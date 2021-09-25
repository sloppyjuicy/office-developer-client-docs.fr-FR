---
title: État nonnitialisé
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f2c2d31033ee77e1de581045012be632f15c5dc4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609235"
---
# <a name="uninitialized-state"></a>État nonnitialisé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état Non initialisé est l’état initial dans les objets de formulaire d’état qui doivent se trouve lors de leur première création. Les objets de formulaire sont initialisés avec les données de message lorsqu’une application cliente appelle la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) sur l’objet de formulaire. Le tableau suivant décrit les transitions autorisées à partir de l’état Unitialized. 
  
|**Méthode IPersistMessage**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Chargez l’objet de formulaire avec les données par défaut.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Chargez l’objet de formulaire avec les données du message cible.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Renvoyer la réussite ou définir la dernière erreur sur et renvoyer E_UNEXPECTED.  <br/> |Nonnitialisé  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur.  <br/> |Nonnitialisé  <br/> |
|Autres [méthodes IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) à partir d’autres interfaces  <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.  <br/> |Nonnitialisé  <br/> |
   
## <a name="see-also"></a>Voir aussi



[État normal](normal-state.md)
  
[États de formulaire](form-states.md)

