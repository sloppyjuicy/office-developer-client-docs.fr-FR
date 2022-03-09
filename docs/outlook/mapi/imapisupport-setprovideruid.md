---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
ms.openlocfilehash: 50f4468d8d35761f680588e81b5b0b285476fed1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368607"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit une structure [MAPIUID](mapiuid.md) qui représente de manière unique le fournisseur de services. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpProviderID_
  
> [in] Pointeur vers la structure **MAPIUID** qui identifie le carnet d’adresses ou le fournisseur de magasin de messages. 
    
 _ulFlags_
  
> Réservé ; doit être zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La structure **MAPIUID** a été inscrite avec succès. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::SetProviderUID** est implémentée pour les objets de prise en charge du carnet d’adresses et du fournisseur de magasins de messages. Ces fournisseurs **appellent SetProviderUID** pour inscrire un identificateur unique décrit dans la structure **MAPIUID** pointée par  _lpProviderID_. Les fournisseurs incluent cet identificateur dans tous les identificateurs d’entrée qu’ils créent. 
  
MAPI utilise la structure **MAPIUID** lorsqu’il envoie des messages sortants au spouleur MAPI et pour déterminer le fournisseur approprié pour la gestion des demandes client. Par exemple, lorsqu’un client appelle la méthode [IMAPISession::OpenEntry](imapisession-openentry.md), MAPI examine la partie **MAPIUID** de l’identificateur d’entrée, la maie au fournisseur qui l’a passée à **SetProviderUID** et appelle l’OpenEntry de ce fournisseur. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

**Appelez SetProviderUID** au moment de l’inscription pour inscrire votre structure **MAPIUID**. MAPI permet aux fournisseurs de carnet d’adresses et de magasin de messages d’inscrire plusieurs identificateurs. Lorsque vous faites plusieurs appels à **SetProviderUID**, il ajoute toujours la structure **MAPIUID** à l’ensemble de structures **MAPIUID** du fournisseur, même si **mapIUID** est un doublon. **SetProviderUID ne** peut pas supprimer **un MAPIUID**. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

