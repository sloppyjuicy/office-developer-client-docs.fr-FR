---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: 311d055e0a319ec26cdc4eba5ac3b50dc9e63d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565178"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Fournit des informations supplémentaires sur la dernière erreur.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Fourni par :  <br/> |Client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Obtient une chaîne de message de l’erreur spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette interface fournit des informations supplémentaires sur une erreur dans [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)et [IOlkAccount](iolkaccount.md). Il est également l’interface de base pour **IOlkAccountManager**, **IOlkAccountNotify**et **IOlkAccount**. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

