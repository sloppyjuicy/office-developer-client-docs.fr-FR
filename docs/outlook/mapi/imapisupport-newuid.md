---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330197"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une nouvelle structure [MAPIUID](mapiuid.md) à utiliser comme identificateur unique. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Paramètres

 _lpMuid_
  
> Pointeur vers la nouvelle structure **MAPIUID** . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La nouvelle structure **MAPIUID** a été créée. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: NewUID** est implémentée pour tous les objets de prise en charge. Les fournisseurs de services et les services de messagerie appellent **NewUID** chaque fois qu'ils ont besoin de générer un identificateur unique à long terme. Un fournisseur de banque de messages, par exemple, peut appeler **NewUID** pour obtenir un **MAPIUID** à placer dans la propriété **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) d'un message nouvellement créé.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Ne confondez pas la structure **MAPIUID** que vous enregistrez à l'ouverture de session avec les structures **MAPIUID** créées par la méthode **NewUID** . La structure **MAPIUID** que vous enregistrez lorsque vous appelez la méthode [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) représente votre carnet d'adresses ou votre fournisseur de banque de messages dans MAPI et est utilisé pour distinguer les identificateurs d'entrée créés par différents fournisseurs. Cette structure **MAPIUID** doit être codée en dur et non obtenue via un appel à **NewUID**.
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

