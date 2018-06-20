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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f16585a96164835784bfa1af3752bd652daf76e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784106"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**S’applique à**: Outlook 
  
Reçoit des notifications à partir de formulaires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Affichage des objets de récepteur de notification  <br/> |
|Implémentée par :  <br/> |Visionneuses de formulaire  <br/> |
|Appelée par :  <br/> |Objets de formulaire  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Type de pointeur :  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Avertit la visionneuse de formulaire fermeture d’un formulaire.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Indique la visionneuse de formulaire à une nouvelle ou un message existant a été chargé dans un formulaire.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Avertit l’utilisateur du formulaire de l’état d’impression d’un formulaire.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Indique que le message en cours a été soumis au spouleur MAPI à la visionneuse de formulaire.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Avertit la visionneuse de formulaire le message actuel dans un formulaire a été enregistré.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

