---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Représente les paramètres de transport que Outlook utilise pour déterminer les tâches de synchronisation nécessaires et pour désactiver les éléments d’interface utilisateur que le compte ne prend pas en charge.
ms.openlocfilehash: 5acfff039d4e8ed7109a8396a6294df096604805
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631217"
---
# <a name="prop_mapi_transport_flags"></a>PROP_MAPI_TRANSPORT_FLAGS

Représente les paramètres de transport que Outlook utilise pour déterminer les tâches de synchronisation nécessaires et pour désactiver les éléments d’interface utilisateur que le compte ne prend pas en charge.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Identificateur :  <br/> |0x2010  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x20100102  <br/> |
|Accès :  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez ou définissez cette propriété à l’aide [d’IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivement.
  
Renvoie **MAPIACCT_SEND_ONLY** si le compte peut uniquement envoyer des messages mais ne peut pas recevoir de messages. Dans ce cas, Outlook l’interface utilisateur qui ne s’applique pas à ce type de comptes (par exemple, l’interface utilisateur pour **l’envoi/réception**).
  
## <a name="see-also"></a>Consultez aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

