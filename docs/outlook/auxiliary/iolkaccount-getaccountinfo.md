---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtient les informations de type et les catégories pour le compte spécifié.
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782645"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Obtient les informations de type et les catégories pour le compte spécifié.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Paramètres

_pclsidType_
  
> [out] L’identificateur de classe pour le type de compte. La valeur doit être une des opérations suivantes :
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out] Le nombre de catégories dans _prgclsidCategory_.
    
_prgclsidCategory_
  
> [out] Tableau des catégories qui est associé à ce compte. Le tableau est de taille * _pcCategories_. La valeur de chaque catégorie dans le tableau doit être une des options suivantes :
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Note

Une fois cette méthode renvoie, vous devez libérer *prgclsidCategory* à l’aide de [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
**IOlkAccount::GetAccountInfo** ne prend pas en charge la catégorie de carnet d’adresses d’un compte Exchange. Si le compte est un échange compte (*pclsidType* **CLSID_OlkMAPIAccount** ) et le compte implémente le carnet d’adresses, appel **IOlkAccount::GetAccountInfo** ne renvoie pas **CLSID_OlkAddressBook** comme une catégorie de * prgclsidCategory* . 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

