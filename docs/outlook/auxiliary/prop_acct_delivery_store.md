---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Représente l’ID d’entrée de la banque de remise par défaut pour le compte.
ms.openlocfilehash: aec2e379c97b8d1088b86c0d663c177b23f042cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601211"
---
# <a name="prop_acct_delivery_store"></a>PROP_ACCT_DELIVERY_STORE

Représente l’ID d’entrée de la banque de remise par défaut pour le compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0018  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x00180102  <br/> |
|Accès :  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez ou définissez cette propriété à l’aide [d’IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp,](iolkaccount-setprop.md)respectivement.
  
L’un des effets secondaires de la définition d’une banque en tant que banque de remise par défaut pour un compte est que lors du démarrage de Outlook, Outlook crée des dossiers de recherche pour cette banque s’ils n’existent pas déjà et liste la banque dans la barre To-Do.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

