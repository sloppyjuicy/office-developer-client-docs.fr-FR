---
title: État non initialisé
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360500"
---
# <a name="uninitialized-state"></a>État non initialisé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'état non initialisé est les objets de formulaire d'état initial doivent se trouver lors de leur création initiale. Les objets Form sont initialisés avec les données de message lorsqu'une application cliente appelle la méthode [IPersistMessage:: InitNew](ipersistmessage-initnew.md) ou [IPersistMessage:: Load](ipersistmessage-load.md) sur l'objet Form. Le tableau suivant décrit les transitions autorisées à partir de l'État unitialized. 
  
|**Méthode IPersistMessage**|**Action**|**Nouvel État**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Charge l'objet Form avec les données par défaut.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Charge l'objet Form avec les données du message cible.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Renvoyer la valeur Success ou définir la dernière erreur sur et renvoyer E_UNEXPECTED.  <br/> |Non initialisée  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur.  <br/> |Non initialisée  <br/> |
|Autres [IPersistMessage:](ipersistmessageiunknown.md) méthodes ou méthodes IUnknown à partir d'autres interfaces  <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.  <br/> |Non initialisée  <br/> |
   
## <a name="see-also"></a>Voir aussi



[État normal](normal-state.md)
  
[États de formulaire](form-states.md)

