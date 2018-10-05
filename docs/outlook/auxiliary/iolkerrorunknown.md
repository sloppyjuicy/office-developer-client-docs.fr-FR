---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: dc2fe6bbaf4515d5c5f5be694b15040bf03ef374
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384639"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Fournit des informations supplémentaires sur la dernière erreur.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
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

