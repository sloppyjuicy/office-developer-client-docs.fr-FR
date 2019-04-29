---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429417"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Reçoit des notifications des formulaires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Exposé par:  <br/> |Afficher les objets du récepteur de notifications  <br/> |
|Implémenté par :  <br/> |Visionneuses de formulaires  <br/> |
|Appelé par :  <br/> |Objets de formulaires  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Type de pointeur:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Avertit la visionneuse de formulaires qu'un formulaire est en cours de fermeture.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Avertit la visionneuse de formulaires qu'un nouveau message ou un message existant a été chargé dans un formulaire.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Avertit la visionneuse de formulaires de l'état d'impression d'un formulaire.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Avertit la visionneuse de formulaires que le message actif a été envoyé au spouleur MAPI.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Avertit la visionneuse de formulaires que le message actif d'un formulaire a été enregistré.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

