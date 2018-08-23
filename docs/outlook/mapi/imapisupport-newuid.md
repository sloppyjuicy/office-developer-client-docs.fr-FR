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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 244087c41e33e470c42434e9d57cee7317bcb78c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571688"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée une nouvelle structure [MAPIUID](mapiuid.md) pour être utilisé comme un identificateur unique. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Paramètres

 _lpMuid_
  
> Pointeur vers la nouvelle structure **MAPIUID** . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La nouvelle structure **MAPIUID** a été créée. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::NewUID** est implémentée pour tous les objets de prise en charge. Fournisseurs de services et les services de messagerie appellent **NewUID** chaque fois qu’ils ont besoin de générer un identificateur unique à long terme. Un message banque fournisseur, par exemple, peut appeler **NewUID** pour obtenir un **MAPIUID** dans la propriété **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) d’un message nouvellement créé.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Ne confondez pas la structure **MAPIUID** que vous inscrivez au moment de l’ouverture de session avec la méthode **NewUID** crée les structures de **MAPIUID** . La structure **MAPIUID** que vous enregistrez lorsque vous appelez la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) représente votre carnet d’adresses ou message stocker fournisseur MAPI et est utilisé pour distinguer les identificateurs d’entrée qui créent des fournisseurs différents. Cette structure **MAPIUID** doit être codées en dur et pas obtenue par un appel à **NewUID**.
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

