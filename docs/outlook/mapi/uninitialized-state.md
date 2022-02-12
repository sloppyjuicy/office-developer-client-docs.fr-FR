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
ms.openlocfilehash: 5faa0d7680b2be561f97741e7898a15321202551
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774761"
---
# <a name="uninitialized-state"></a>État nonnitialisé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état Non initialisé est l’état initial dans les objets de formulaire d’état qui doivent se trouve lors de leur première création. Les objets de formulaire sont initialisés avec les données de message lorsqu’une application cliente appelle la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) sur l’objet de formulaire. Le tableau suivant décrit les transitions autorisées à partir de l’état Unitialized. 
  
|**Méthode IPersistMessage**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Chargez l’objet de formulaire avec les données par défaut. |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Chargez l’objet de formulaire avec les données du message cible. |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Renvoyer la réussite ou définir la dernière erreur sur et renvoyer E_UNEXPECTED. |Nonnitialisé  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur. |Nonnitialisé  <br/> |
|Autres [méthodes IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) à partir d’autres interfaces  <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED. |Nonnitialisé  <br/> |
   
## <a name="see-also"></a>Voir aussi



[État normal](normal-state.md)
  
[États de formulaire](form-states.md)

