---
title: État noScribble
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326200"
---
# <a name="noscribble-state"></a>État noScribble

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'État noScribble indique que les modifications apportées à un message sont enregistrées. L'enregistrement effectif des valeurs stockées dans l'interface utilisateur de l'objet Form se produit lorsque la méthode [IPersistMessage:: Save](ipersistmessage-save.md) de l'objet Form est appelée par l'application cliente. Le tableau suivant décrit les transitions autorisées à partir de l'État noScribble. 
  
|IPersistMessage * * méthode * *|**Action**|**Nouvel État**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage = =_ null)  <br/> |Si l'indicateur _fSameAsLoad_ était true sur l'appel [IPersistMessage:: Save](ipersistmessage-save.md) qui a entraîné l'entrée de l'état de l'option noscribbler dans le formulaire et que le message a été modifié, marquez en interne les modifications comme enregistrées et appelez la [IMAPIViewAdviseSink:: OnSaved](imapiviewadvisesink-onsaved.md) procédé.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage:: SaveCompleted** (_pMessage! =_ null)  <br/> |Appelez la méthode [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) (similaire à la méthode OLE [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) ) suivie des actions **SaveCompleted** normales. Si **SaveCompleted** a réussi, entrez l'état normal. Dans le cas contraire, entrez l'état [HandsOffAfterSave](handsoffaftersave-state.md) .  <br/> |Normal ou HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Appelez de manière récursive la méthode **HandsOffMessage** sur les messages incorporés ou la méthode OLE **IPersistStorage:: HandsOffStorage** sur les objets OLE incorporés. Libérez l'objet message et tous les messages ou objets incorporés.  <br/> |HandsOffAfterSave  <br/> |
|**Save**, [IPersistMessage:: InitNew](ipersistmessage-initnew.md)ou [IPersistMessage:: Load](ipersistmessage-load.md) <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoyer la dernière erreur.  <br/> |NoScribble  <br/> |
|Autres [IPersistMessage:](ipersistmessageiunknown.md) méthodes ou méthodes IUnknown à partir d'autres interfaces  <br/> |Définissez la dernière erreur sur et renvoyez E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

