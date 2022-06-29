---
title: IOlkEnum
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 04c75b39806a6211fe3d394e91715806bed0d1e4
ms.sourcegitcommit: 1da753936975e64349cbd6954cf1c1732289a0b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2022
ms.locfileid: "66448593"
---
# <a name="iolkenum"></a>IOlkEnum

Prend en charge l’énumération de comptes en tant qu’objets [IUnknown](/cpp/atl/iunknown) . 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Hérite de :  |[Iunknown](/cpp/atl/iunknown) |
|Implémenté par : |Outlook  |
|Fourni par :    |[IOlkAccountManager::EnumerateAccounts](iolkaccountmanager-enumerateaccounts.md)  |
|Appelé par :      |Client  |
|Identificateur d’interface : |IID_IOlkEnum  |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Membre |Valeur |
|:-----|:-----|
|[GetCount](iolkenum-getcount.md) |Obtient le nombre de comptes dans l’énumérateur. |
|[Reset](iolkenum-reset.md)  |Réinitialise l’énumérateur au début. |
|[GetNext](iolkenum-getnext.md) |Obtient le compte suivant dans l’énumérateur. |
|[Skip](iolkenum-skip.md) |Ignore un nombre spécifié de comptes dans l’énumérateur. |
   
## <a name="remarks"></a>Remarques

Cette interface est retournée par **IOlkAccountManager::EnumerateAccounts** lors de l’obtention d’un énumérateur de comptes. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
