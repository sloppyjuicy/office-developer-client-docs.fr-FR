---
title: État normal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335741"
---
# <a name="normal-state"></a>État normal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'état normal est l'endroit où l'objet Form consacre la plus grande partie de son temps, en attendant que les applications clientes lancent une action telle que l'enregistrement des modifications ou la fermeture du formulaire. Le tableau suivant décrit les transitions autorisées par rapport à l'état normal.
  
|**Méthode IPersistMessage**|**Action**|**Nouvel État**|
|:-----|:-----|:-----|
|[IPersistMessage:: enregistrer](ipersistmessage-save.md) (_pMessage = =_ null, _fSameAsLoad = =_ true)  <br/> - ou -  <br/> **IPersistMessage:: enregistrer** (_pMessage! =_ null, _fSameAsLoad = =_ false)  <br/> |Enregistrer de manière récursive tous les objets OLE incorporés qui ont été modifiés. Enregistrer les données de message dans l'objet message. Stockez l'indicateur _fSameAsLoad_ pour une utilisation ultérieure dans l'État noscribble. [](noscribble-state.md)  <br/> |NoScribble  <br/> |
|**IPersistMessage:: enregistrer** (_pMessage! =_ null, _fSameAsLoad = =_ true)  <br/> |Il s'agit du même que pour le cas précédent, sauf que cet appel **enregistré** est utilisé dans des situations de mémoire insuffisante et qu'il ne doit pas échouer en cas de manque de mémoire.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Appelez de manière récursive la méthode **HandsOffMessage** sur les messages incorporés ou la méthode OLE [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) sur les objets OLE incorporés. Libérez l'objet message et tous les messages ou objets incorporés.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md) ou [IPersistMessage:: Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur.  <br/> |Normal  <br/> |
|Autres [IPersistMessage:](ipersistmessageiunknown.md) méthodes ou méthodes IUnknown à partir d'autres interfaces  <br/> |Implémentez comme décrit dans la documentation de l'interface [IPersistMessage: IUnknown](ipersistmessageiunknown.md) .  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

