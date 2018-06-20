---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2182ec71c54c81e9a43a34973e005292ddccdfff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784038"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**S’applique à**: Outlook 
  
Enregistre une structure [MAPIUID](mapiuid.md) qui représente le fournisseur de services de manière unique. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpProviderID_
  
> [in] Pointeur vers la structure **MAPIUID** qui identifie le fournisseur de banque de message ou de carnet d’adresses. 
    
 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La structure **MAPIUID** a été enregistrée avec succès. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::SetProviderUID** est implémentée pour adresse livre et message fournisseur prise en charge des objets store. Ces fournisseurs appellent **SetProviderUID** pour inscrire un identificateur unique décrit dans la structure **MAPIUID** qui est indiquée par _lpProviderID_. Fournisseurs d’incluent cet identificateur dans tous les identificateurs d’entrée qu’ils créent. 
  
MAPI utilise la structure **MAPIUID** lorsqu’il envoie les messages sortants pour le spouleur MAPI et pour déterminer le fournisseur approprié pour la gestion des demandes des clients. Par exemple, lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md) , examine la partie **MAPIUID** de l’identificateur d’entrée MAPI, est mappé au fournisseur qui transmis aux **SetProviderUID**et appelle de ce fournisseur **OpenEntry** . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appelez **SetProviderUID** au moment de l’ouverture de session pour inscrire votre structure **MAPIUID** . MAPI permet adresse livre et message fournisseurs de magasins inscrire plusieurs identificateurs. Lorsque vous effectuez plusieurs appels vers **SetProviderUID**, ajoute toujours la structure **MAPIUID** pour l’ensemble du fournisseur de structures **MAPIUID** , même si le **MAPIUID** est un doublon. Impossible de supprimer un **MAPIUID** **SetProviderUID** . 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

