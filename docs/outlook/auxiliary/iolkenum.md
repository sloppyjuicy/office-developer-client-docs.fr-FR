---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389735"
---
# <a name="iolkenum"></a>IOlkEnum

Prend en charge l’énumération des comptes en tant qu’objets [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) . 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Fourni par :  <br/> |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md) <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IOlkEnum  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) <br/> |Obtient le nombre de comptes dans l’énumérateur.  <br/> |
|[Reset](iolkenum-reset.md) <br/> |Réinitialise l’énumérateur au début.  <br/> |
|[GetNext](iolkenum-getnext.md) <br/> |Obtient le compte suivant dans l’énumérateur.  <br/> |
|[Ignorer](iolkenum-skip.md) <br/> |Ignore un nombre spécifié de comptes dans l’énumérateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette interface est retournée par **IOlkAccountManager::EnumerateAccounts** lors de l’obtention d’un énumérateur de comptes. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

