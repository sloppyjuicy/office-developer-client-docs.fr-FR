---
title: État normal
description: L’état Normal est l’endroit où l’objet de formulaire passe la majeure partie de son temps, en attendant que les applications clientes lancent une action, comme l’enregistrement des modifications ou la fermeture d’un formulaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
ms.openlocfilehash: ca22ac875450a58131e1ffd09daec3673d3e396a
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852970"
---
# <a name="normal-state"></a>État normal

**S’applique à** : Outlook 2013 | Outlook 2016
  
L’état Normal est l’endroit où l’objet de formulaire passe la majeure partie de son temps, en attendant que les applications clientes lancent une action telle que l’enregistrement des modifications ou la fermeture du formulaire. Le tableau suivant décrit les transitions autorisées à partir de l’état Normal.
  
|**IPersistMessage, méthode**|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL, _fSameAsLoad ==_ TRUE)  <br/> - ou -  <br/> **IPersistMessage::Save**(_pMessage !=_ NULL, _fSameAsLoad ==_ FALSE)  <br/> |Enregistrez de manière récursive tous les objets OLE incorporés qui ont été modifiés. Enregistrez les données de message dans l’objet de message. Stockez l’indicateur _fSameAsLoad_ pour une utilisation ultérieure dans l’état [NoScribble](noscribble-state.md) . |NoScribble  <br/> |
|**IPersistMessage::Save**(_pMessage !=_ NULL, _fSameAsLoad ==_ TRUE)  <br/> |Il s’agit du même que dans le cas précédent, sauf que cet appel **d’enregistrement** est utilisé dans des situations de mémoire insuffisante et ne doit pas échouer en raison d’un manque de mémoire. |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Appeler de manière **récursive la méthode HandsOffMessage sur les messages incorporés** ou la méthode OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) sur les objets OLE incorporés. Libérez l’objet de message et tous les messages ou objets incorporés. |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur sur et retournez E_UNEXPECTED. |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retourne la dernière erreur. |Normal  <br/> |
|Autres [IPersistMessage : méthodes ou méthodes IUnknown](ipersistmessageiunknown.md) provenant d’autres interfaces  <br/> |Implémentez comme décrit dans la documentation de l’interface [IPersistMessage : IUnknown](ipersistmessageiunknown.md) . |Normal  <br/> |

## <a name="see-also"></a>Voir aussi

[États de formulaire](form-states.md)
