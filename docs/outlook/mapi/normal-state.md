---
title: État normal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a7aa3edf949cbbf86f61478253b29366d596e123
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778810"
---
# <a name="normal-state"></a>État normal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’état Normal est l’endroit où l’objet de formulaire passe la plupart de son temps, en attendant que les applications clientes lancent une action telle que l’enregistrement des modifications ou la fermeture du formulaire. Le tableau suivant décrit les transitions autorisées à partir de l’état Normal.
  
|**Méthode IPersistMessage**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> - ou -  <br/> **IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)  <br/> |Enregistrez de manière récursive tous les objets OLE incorporés qui ont été modifiés. Enregistrez de nouveau les données de message dans l’objet message. Stockez  _l’indicateur fSameAsLoad_ pour une utilisation ultérieure dans [l’état NoScribble](noscribble-state.md) . |NoScribble  <br/> |
|**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> |Ceci est identique au cas précédent, sauf que cet appel d’enregistrer est utilisé dans des situations de mémoire faible et ne doit pas échouer en raison d’un manque de mémoire. |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Appeler de manière **récursive la méthode HandsOffMessage** sur les messages incorporés ou la méthode OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) sur des objets OLE incorporés. Relâchez l’objet message et tous les messages ou objets incorporés. |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED. |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur. |Normal  <br/> |
|Autres [méthodes IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) à partir d’autres interfaces  <br/> |Implémenter comme décrit dans la documentation [pour l’interface IPersistMessage : IUnknown](ipersistmessageiunknown.md) . |Normal  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

