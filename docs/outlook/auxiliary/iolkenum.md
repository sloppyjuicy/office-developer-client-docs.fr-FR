---
title: IOlkEnum
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 7fc5bf5db4aed337c697163cd4b340b44af49845
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631224"
---
# <a name="iolkenum"></a>IOlkEnum

Prend en charge l’éumation des comptes en tant [qu’objets IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown.md) . 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Hérite de :  |[IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown.md) |
|Implémenté par : |Outlook  |
|Fourni par :    |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md)  |
|Appelé par :      |Client  |
|Identificateur d’interface : |IID_IOlkEnum  |
   
## <a name="vtable-order"></a>Ordre des vtables

|Membre |Valeur |
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) |Obtient le nombre de comptes dans l’éumérateur. |
|[Reset](iolkenum-reset.md)  |Réinitialise l’éumérateur au début. |
|[GetNext](iolkenum-getnext.md) |Obtient le compte suivant dans l’éumérateur. |
|[Skip](iolkenum-skip.md) |Ignore un nombre spécifié de comptes dans l’éumérateur. |
   
## <a name="remarks"></a>Remarques

Cette interface est renvoyée par **IOlkAccountManager::EnumerateAccounts** lors de l’obtention d’un éumérateur de comptes. 
  
## <a name="see-also"></a>Consultez aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
