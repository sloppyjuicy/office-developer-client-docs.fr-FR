---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: e18d23847744425bd7feb62dd615a4dcfa1c9287
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625643"
---
# <a name="iolkenum"></a>IOlkEnum

Prend en charge l’éumation des comptes en tant [qu’objets IUnknown.](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Fourni par :  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Obtient le nombre de comptes dans l’éumérateur.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Réinitialise l’éumérateur au début.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Obtient le compte suivant dans l’éumérateur.  <br/> |
|[Skip](iolkenum-skip.md) <br/> |Ignore un nombre spécifié de comptes dans l’éumérateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette interface est renvoyée par **IOlkAccountManager::EnumerateAccounts** lors de l’obtention d’un éumérateur de comptes. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

