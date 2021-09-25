---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: 60e5a6f7400a3bb7ab2df1fc25cc2c469af29418
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617082"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Fournit des informations supplémentaires sur la dernière erreur.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|Fourni par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IOlkErrorUnknown  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Obtient une chaîne de message pour l’erreur spécifiée.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette interface fournit des informations supplémentaires sur une erreur dans [IOlkAccountManager,](iolkaccountmanager.md) [IOlkAccountNotify](iolkaccountnotify.md)et [IOlkAccount](iolkaccount.md). Il s’agit également de l’interface de base pour **IOlkAccountManager,** **IOlkAccountNotify** et **IOlkAccount**. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

