---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 33d811af0fc9e06902750075ba39bfb6ca88903f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593710"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Transmet le fournisseur de banque comme un champ de la structure MAPISIB pendant un appel à [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md). Le fournisseur de banque utilise cette interface pour fournir des commentaires à Microsoft Outlook sur l’état de la synchronisation.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> ||
|Exposés par :  <br/> |Outlook  <br/> |
|Implémentée par :  <br/> |Outlook  <br/> |
|Appelée par :  <br/> |Fournisseurs de magasins  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |Le fournisseur de banque appelle régulièrement cette fonction pour mettre à jour l’état dans la boîte de dialogue d’envoi/réception.  <br/> |
|[Erreur](imapisyncprogresscallback-error.md) <br/> |Si vous rencontrez des erreurs lors de la synchronisation, le fournisseur de banque appelle cette fonction pour fournir plus d’informations qui sont affichent dans la boîte de dialogue d’envoi/réception.  <br/> |
|[Terminé](imapisyncprogresscallback-done.md) <br/> |Le fournisseur de banque appelle cette fonction pour informer Outlook que la synchronisation est terminé.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISync : IUnknown](imapisynciunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

