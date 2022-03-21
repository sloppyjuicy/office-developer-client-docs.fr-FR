---
title: IOlkErrorUnknown
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: 772e01640d76338cac51bcf4483b41c6b84a1991
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628599"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Fournit des informations supplémentaires sur la dernière erreur.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Hérite de :   |[IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown.md) |
|Fourni par :   |Client  |
|Identificateur d’interface :   |IID_IOlkErrorUnknown  |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member | Description |
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Obtient une chaîne de message pour l’erreur spécifiée. |
   
## <a name="remarks"></a>Remarques

Cette interface fournit des informations supplémentaires sur une erreur [dans IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md) et [IOlkAccount](iolkaccount.md). Il s’agit également de l’interface de base pour **IOlkAccountManager**, **IOlkAccountNotify** et **IOlkAccount**. 
  
## <a name="see-also"></a>Consultez aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
