---
title: IOlkErrorUnknown
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: ca9aa0cf52c283a7e91cd29f1e99415db0023ac8
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777592"
---
# <a name="iolkerrorunknown"></a>IOlkErrorUnknown

Fournit des informations supplémentaires sur la dernière erreur.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :   |[IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown.md) |
|Fourni par :   |Client  |
|Identificateur d’interface :   |IID_IOlkErrorUnknown  |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](iolkerrorunknown-getlasterror.md) <br/> |Obtient une chaîne de message pour l’erreur spécifiée. |
   
## <a name="remarks"></a>Remarques

Cette interface fournit des informations supplémentaires sur une erreur [dans IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md) et [IOlkAccount](iolkaccount.md). Il s’agit également de l’interface de base pour **IOlkAccountManager**, **IOlkAccountNotify** et **IOlkAccount**. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
