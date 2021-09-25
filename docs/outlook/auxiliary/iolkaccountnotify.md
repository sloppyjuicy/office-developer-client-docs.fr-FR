---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: 1d9b659cee551140aedd4caf21d929f6df2bfc72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605385"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Fournit un rappel au client pour les modifications apportées à un compte.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Fourni par :  <br/> | Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[Notification](iolkaccountnotify-notify.md) <br/> |Avertit le client des modifications apportées au compte spécifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette interface est transmise à [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) lors de la configuration des notifications. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

