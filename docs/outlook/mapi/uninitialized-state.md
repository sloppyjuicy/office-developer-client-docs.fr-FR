---
title: État non initialisé
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578247"
---
# <a name="uninitialized-state"></a>État non initialisé

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’état non initialisée est le formulaire état initial dans des objets doivent être lors de leur création. Objets de formulaire devient initialisés avec les données de message lorsqu’une application cliente appelle la méthode [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) sur l’objet de formulaire. Le tableau suivant décrit les transitions autorisées à partir de l’état Unitialized. 
  
|**Méthode IPersistMessage**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Chargement de l’objet de formulaire avec des données par défaut.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Chargement de l’objet de formulaire avec des données à partir du message cible.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Renvoyez réussite, ou bien la dernière erreur et E_UNEXPECTED.  <br/> |Non initialisée  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoie la dernière erreur.  <br/> |Non initialisée  <br/> |
|Autres [IPersistMessage : IUnknown](ipersistmessageiunknown.md) méthodes ou autres interfaces  <br/> |Définissez la dernière erreur à et E_UNEXPECTED.  <br/> |Non initialisée  <br/> |
   
## <a name="see-also"></a>Voir aussi



[État normal](normal-state.md)
  
[États de formulaire](form-states.md)

