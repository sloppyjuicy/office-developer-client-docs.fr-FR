---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: Reçoit des notifications à partir de formulaires Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 9fa8add575c371790eb0bedad0d0bf144516730f
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782936"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Reçoit des notifications à partir de formulaires. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Afficher les objets de sink de conseil  <br/> |
|Implémenté par :  <br/> |Visionneuses de formulaires  <br/> |
|Appelé par :  <br/> |Objets de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Type de pointeur :  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Avertit la visionneuse de formulaire qu’un formulaire est en cours de fermeture. |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Avertit la visionneuse de formulaire qu’un nouveau message ou un message existant a été chargé dans un formulaire. |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Avertit la visionneuse de formulaires de l’état d’impression d’un formulaire. |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Avertit la visionneuse de formulaire que le message actuel a été envoyé aupooler MAPI. |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Avertit la visionneuse de formulaire que le message en cours dans un formulaire a été enregistré. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

