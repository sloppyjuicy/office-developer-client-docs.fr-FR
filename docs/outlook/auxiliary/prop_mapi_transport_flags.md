---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Représente les paramètres de transport qu'Outlook utilise pour déterminer les tâches de synchronisation nécessaires et pour désactiver les éléments d'interface utilisateur non pris en charge par le compte.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404525"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Représente les paramètres de transport qu'Outlook utilise pour déterminer les tâches de synchronisation nécessaires et pour désactiver les éléments d'interface utilisateur non pris en charge par le compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x2010  <br/> |
|Type de propriété:  <br/> |PT_BINARY  <br/> |
|Balise de propriété:  <br/> |0x20100102  <br/> |
|Access  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenir ou définir cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md) ou [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivement.
  
Renvoie **MAPIACCT_SEND_ONLY** si le compte peut uniquement envoyer des messages mais ne peut pas recevoir de messages. Dans ce cas, Outlook désactive l'interface utilisateur qui ne s'applique pas à ce type de comptes (par exemple, l'interface utilisateur pour l' **envoi et la réception**).
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

