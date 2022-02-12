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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f67b5330c78bfd2c4bbb6beef53d78b347b2fcc3
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776346"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Reçoit des notifications à partir de formulaires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Afficher les objets de sink de conseil  <br/> |
|Implémenté par :  <br/> |Visionneuses de formulaires  <br/> |
|Appelé par :  <br/> |Objets de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Type de pointeur :  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Avertit la visionneuse de formulaire qu’un formulaire est en cours de fermeture. |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Avertit la visionneuse de formulaire qu’un nouveau message ou un message existant a été chargé dans un formulaire. |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Avertit la visionneuse de formulaires de l’état d’impression d’un formulaire. |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Avertit la visionneuse de formulaire que le message actuel a été envoyé aupooler MAPI. |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Avertit la visionneuse de formulaire que le message en cours dans un formulaire a été enregistré. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

