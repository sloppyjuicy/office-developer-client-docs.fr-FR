---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: 0ff1fb7e2b59325a55c0000d04a607ec8e1fd012
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63783153"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Fournit un rappel au client pour les modifications apportées à un compte.
  
## <a name="quick-info"></a>Informations rapides

|Propriété|Valeur|
|:-----|:-----|
|Hérite de :  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Fourni par :  <br/> | Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member|Description|
|:-----|:-----|
|[Notification](iolkaccountnotify-notify.md) <br/> |Avertit le client des modifications apportées au compte spécifié. |
   
## <a name="remarks"></a>Remarques

Cette interface est transmise à [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) lors de la configuration des notifications. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

