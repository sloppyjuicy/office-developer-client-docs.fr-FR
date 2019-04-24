---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322098"
---
# <a name="iolkenum"></a>IOlkEnum

Prend en charge l'énumération des comptes en tant qu'objets [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) . 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de:  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Fourni par :  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur de l'interface:  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Obtient le nombre de comptes dans l'énumérateur.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Rétablit l'énumérateur au début.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Obtient le compte suivant dans l'énumérateur.  <br/> |
|[Skip](iolkenum-skip.md) <br/> |Ignore un nombre spécifié de comptes dans l'énumérateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette interface est renvoyée par **IOlkAccountManager:: EnumerateAccounts** lors de l'obtention d'un énumérateur de comptes. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

