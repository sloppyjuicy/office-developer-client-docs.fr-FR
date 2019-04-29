---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: ab24feca84e7049a9800b860c332db52d19cf929
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412498"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Fournit un rappel au client pour les modifications apportées à un compte.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Fourni par :  <br/> | Client  <br/> |
|Identificateur de l'interface:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Avertir](iolkaccountnotify-notify.md) <br/> |Avertit le client des modifications apportées au compte spécifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Cette interface est transmise à [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md) lors de la configuration des notifications. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

