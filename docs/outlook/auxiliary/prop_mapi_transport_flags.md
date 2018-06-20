---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Représente les paramètres de transport Outlook utilise pour déterminer les tâches de synchronisation et pour désactiver les éléments de l’interface utilisateur du compte ne prenant pas en charge.
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782815"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Représente les paramètres de transport Outlook utilise pour déterminer les tâches de synchronisation et pour désactiver les éléments de l’interface utilisateur du compte ne prenant pas en charge.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x2010  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x20100102  <br/> |
|Access :  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenir ou définir cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivement.
  
Renvoie **MAPIACCT_SEND_ONLY** si le compte peut uniquement envoyer des messages, mais ne peut pas recevoir de messages. Dans ce cas, Outlook désactive l’interface utilisateur qui ne s’applique pas à ce type de compte (par exemple, l’interface utilisateur pour **l’Envoi/réception**).
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

