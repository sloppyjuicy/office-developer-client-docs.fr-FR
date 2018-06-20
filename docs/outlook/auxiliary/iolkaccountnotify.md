---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: f4b57ad1062df9aa1809e8eb422a2c983adcac4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782734"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Fournit un rappel au client pour les modifications à un compte.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Fourni par :  <br/> | Client  <br/> |
|Identificateur de l’interface :  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Avertir](iolkaccountnotify-notify.md) <br/> |Notifie le client des modifications apportées au compte spécifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette interface est transmise à [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) lors de la configuration des notifications. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

