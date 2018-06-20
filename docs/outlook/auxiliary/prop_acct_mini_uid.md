---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Retourne un identificateur de compte qui est unique pour les profils Outlook.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782813"
---
# <a name="propacctminiuid"></a>PROP_ACCT_MINI_UID

Retourne un identificateur de compte qui est unique pour les profils Outlook.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0003  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Balise de propriété :  <br/> |0x00030003  <br/> |
|Access :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md). Si le client essaie de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**. 
  
Cette propriété est différente de [PROP_ACCT_ID](prop_acct_id.md) dans la mesure où sa valeur identifie le compte au sein et en dehors du profil dans lequel le compte a été créé, tandis que **PROP_ACCT_ID** est unique seulement parmi tous les comptes au sein d’un profil dans lequel le compte a été créé. Lorsqu’un message avec ces propriétés se déplace sur un deuxième ordinateur avec un autre profil Outlook et un ensemble différent de comptes, **PROP_ACCT_MINI_UID** peuvent identifier le compte d’origine dans le profil d’origine. Toutefois, **PROP_ACCT_ID** peut éventuellement entre en conflit avec un compte dans le profil de l’ordinateur. 
  
## <a name="see-also"></a>Voir aussi

- [PROP_ACCT_ID](prop_acct_id.md)  
- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

