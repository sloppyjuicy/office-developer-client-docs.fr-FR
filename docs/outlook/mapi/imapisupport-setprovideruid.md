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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437538"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit une structure [MAPIUID](mapiuid.md) qui représente le fournisseur de services de manière unique. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpProviderID_
  
> dans Pointeur vers la structure **MAPIUID** qui identifie le carnet d'adresses ou le fournisseur de banque de messages. 
    
 _ulFlags_
  
> MSR doit être égal à zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La structure **MAPIUID** a été correctement inscrite. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: SetProviderUID** est implémentée pour les objets de prise en charge du carnet d'adresses et du fournisseur de banque de messages. Ces fournisseurs appellent **SetProviderUID** pour enregistrer un identificateur unique décrit dans la structure **MAPIUID** pointée par _lpProviderID_. Les fournisseurs incluent cet identificateur dans tous les identificateurs d'entrée qu'ils créent. 
  
MAPI utilise la structure **MAPIUID** lorsqu'il envoie des messages sortants vers le spouleur MAPI et détermine le fournisseur approprié pour la gestion des demandes des clients. Par exemple, lorsqu'un client appelle la méthode [IMAPISession:: OpenEntry](imapisession-openentry.md) , MAPI examine la partie **MAPIUID** de l'identificateur d'entrée, la mappe au fournisseur qui l'a passée à **SetProviderUID**et appelle le **OpenEntry** de ce fournisseur. . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **SetProviderUID** au moment de l'ouverture de session pour enregistrer votre structure **MAPIUID** . MAPI permet aux fournisseurs de carnets d'adresses et de banques de messages d'enregistrer plusieurs identificateurs. Lorsque vous effectuez plusieurs appels à **SetProviderUID**, il ajoute toujours la structure **MAPIUID** au jeu de structures **MAPIUID** du fournisseur, même si le **MAPIUID** est un doublon. **SetProviderUID** ne peut pas supprimer un **MAPIUID**. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

