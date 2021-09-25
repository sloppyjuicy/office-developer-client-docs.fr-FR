---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtient les informations de type et de catégorie pour le compte spécifié.
ms.openlocfilehash: 7d5abc2126ff3aa9c66f82d1c104c030f9e029a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567941"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

Obtient les informations de type et de catégorie pour le compte spécifié.
  
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
  
> [out] Identificateur de classe pour le type de compte. La valeur doit être une des opérations suivantes :
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out] Nombre de catégories dans  _prgclsidCategory_.
    
_prgclsidCategory_
  
> [out] Tableau des catégories associées à ce compte. Le tableau est de taille * _pcCategories_. La valeur de chaque catégorie du tableau doit être l’une des suivantes :
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Après le retour de cette méthode, vous devez libérer  *prgclsidCategory*  à l’aide de [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
**IOlkAccount::GetAccountInfo** ne prend pas en charge la catégorie de carnet d’adresses pour Exchange compte. Si le compte est un compte Exchange (*pclsidType* est **CLSID_OlkMAPIAccount** ), et que le compte implémente le carnet d’adresses, l’appel de **IOlkAccount::GetAccountInfo** ne retournera pas **CLSID_OlkAddressBook** en tant que catégorie dans *prgclsidCategory* . 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

