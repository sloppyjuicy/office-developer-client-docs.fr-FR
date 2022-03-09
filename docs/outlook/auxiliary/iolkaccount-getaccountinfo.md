---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtient les informations de type et de catégorie pour le compte spécifié.
ms.openlocfilehash: 7d493552319ed7afc5ca5e30e3a78f8dd47e0e70
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373997"
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
  
> [out] Nombre de catégories dans _prgclsidCategory_.

_prgclsidCategory_
  
> [out] Tableau des catégories associées à ce compte. Le tableau est de taille * _pcCategories_. La valeur de chaque catégorie du tableau doit être l’une des suivantes :

- CLSID_OlkMail

- CLSID_OlkAddressBook

- CLSID_OlkStore

## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Après le retour de cette méthode, vous devez libérer _prgclsidCategory_ à l’aide [d’IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
**IOlkAccount::GetAccountInfo** ne prend pas en charge la catégorie de carnet d’adresses d’Exchange compte. Si le compte est un compte Exchange (_pclsidType_ est **CLSID_OlkMAPIAccount** ), et que le compte implémente le carnet d’adresses, l’appel **d’IOlkAccount::GetAccountInfo** ne retournera pas **CLSID_OlkAddressBook** en tant que catégorie dans _prgclsidCategory_.
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)
