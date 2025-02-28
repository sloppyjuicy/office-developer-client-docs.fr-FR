---
title: IMAPISyncProgressCallback IUnknown
description: IMAPISync ProgressCallbackIUnknown transmet le fournisseur de magasin en tant que champ sur la structure MAPISIB lors d’un appel à IMAPISync SynchronizeInBackground.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
ms.openlocfilehash: 69b61db06348cfc606006ed71773471eb92ef3bd
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827876"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Transmet le fournisseur de magasin en tant que champ sur la structure MAPISIB lors d’un appel à [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md). Le fournisseur de magasin utilise cette interface pour fournir des commentaires à Microsoft Outlook sur l’état de la synchronisation.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> ||
|Exposé par :  <br/> |Outlook  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Fournisseurs du Store  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |Le fournisseur de magasin appelle régulièrement cette fonction pour mettre à jour l’état dans la boîte de dialogue Envoyer/recevoir. |
|[Error](imapisyncprogresscallback-error.md) <br/> |Si des erreurs se produisent lors de la synchronisation, le fournisseur du magasin appelle cette fonction pour fournir les détails affichés dans la boîte de dialogue Envoyer/recevoir. |
|[Terminé](imapisyncprogresscallback-done.md) <br/> |Le fournisseur de magasin appelle cette fonction pour informer Outlook que la synchronisation est terminée. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISync : IUnknown](imapisynciunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

