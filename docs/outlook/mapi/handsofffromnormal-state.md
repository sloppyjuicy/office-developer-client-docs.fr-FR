---
title: État HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d0b7baf4ab17d12145170961a43ca4be252146a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783454"
---
# <a name="handsofffromnormal-state"></a>État HandsOffFromNormal

  
  
**S’applique à**: Outlook 
  
L’état HandsOffFromNormal est très similaire à l’état [HandsOffAfterSave](handsoffaftersave-state.md) . Il fait partie du processus de l’enregistrement du contenu d’un formulaire dans un stockage permanent. Dans cet état, l’objet de formulaire doit ne pas apporter des modifications à la copie en mémoire des valeurs des propriétés du message, car il peut ne pas être une autre possibilité d’enregistrer ces modifications. Le tableau suivant décrit les transitions autorisées à partir de l’état HandsOffFromNormal. 
  
|Méthode IPersistMessage ** **|**Action**|**Nouvel état**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage ! =_ NULL)  <br/> |Remplacer message de l’objet message par _pMessage_, qui est le remplacement du message révoqué par l’appel précédent à [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md). Les données dans le nouveau message sont garanties être le même que dans le message révoqué. Le message ne doit pas être marqué comme nettoyé ni [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) doit être appelée après cet appel. Si l’appel de **méthode SaveCompleted** réussit, entrez l’état [Normal](normal-state.md) . Dans le cas contraire, rester à l’état HandsOffFromNormal.  <br/> |Normal ou HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ==_ NULL)  <br/> |La valeur la dernière erreur E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |La valeur la dernière erreur E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoie la dernière erreur.  <br/> |HandsOffFromNormal  <br/> |
|Autres [IPersistMessage : IUnknown](ipersistmessageiunknown.md) méthodes ou autres interfaces  <br/> |La valeur la dernière erreur E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Voir aussi



[États de formulaire](form-states.md)

