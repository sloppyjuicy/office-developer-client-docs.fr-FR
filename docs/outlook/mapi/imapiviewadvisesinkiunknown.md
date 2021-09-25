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
ms.openlocfilehash: b7486139818ede9bd7e4b66472317ab50b05ba4d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567374"
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
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Avertit la visionneuse de formulaires qu’un formulaire est en cours de fermeture.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Avertit la visionneuse de formulaire qu’un nouveau message ou un message existant a été chargé dans un formulaire.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Avertit la visionneuse de formulaires de l’état d’impression d’un formulaire.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Avertit la visionneuse de formulaire que le message actuel a été envoyé aupooler MAPI.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Avertit la visionneuse de formulaire que le message en cours dans un formulaire a été enregistré.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

