---
title: IMAPISyncProgressCallback IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e96252a4bb95989f42c381b7387f20d909da7dcc
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63722854"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Transmet le fournisseur de magasin en tant que champ sur la structure MAPISIB pendant un appel à [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md). Le fournisseur du Store utilise cette interface pour fournir des commentaires à Microsoft Outlook sur l’état de la synchronisation.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> ||
|Exposé par :  <br/> |Outlook  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Appelé par :  <br/> |Fournisseurs du Store  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |Le fournisseur de magasins appelle régulièrement cette fonction pour mettre à jour l’état dans la boîte de dialogue d’envoi/réception. |
|[Erreur](imapisyncprogresscallback-error.md) <br/> |Si des erreurs se sont rencontrées lors de la synchronisation, le fournisseur de magasins appelle cette fonction pour fournir des détails affichés dans la boîte de dialogue d’envoi/réception. |
|[Terminé](imapisyncprogresscallback-done.md) <br/> |Le fournisseur de magasin appelle cette fonction pour Outlook que la synchronisation est terminée. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISync : IUnknown](imapisynciunknown.md)


[Interfaces MAPI](mapi-interfaces.md)

