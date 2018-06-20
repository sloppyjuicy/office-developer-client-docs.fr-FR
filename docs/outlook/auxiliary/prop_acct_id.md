---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Retourne un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782812"
---
# <a name="propacctid"></a>PROP_ACCT_ID

Retourne un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0001  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Balise de propriété :  <br/> |0 x 00010003  <br/> |
|Access :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à l’aide de [IOlkAccount::GetProp](iolkaccount-getprop.md). Si le client essaie de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**. 
  
Cette propriété est différente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) dans la mesure où sa valeur est unique seulement parmi tous les comptes dans ce profil dans lequel le compte a été créé, tandis que **propriétés\_ACCT_MINI_UID** identifie de manière unique le compte et à l’extérieur du profil dans lequel le compte a été créé. Lorsqu’un message avec ces propriétés se déplace sur un deuxième ordinateur avec un autre profil Outlook et un ensemble différent de comptes, **PROP_ACCT_ID** peut éventuellement entrer en conflit avec un compte dans le profil du deuxième ordinateur et **PROP_ACCT_MINI_UID** peuvent identifier le compte d’origine dans le profil d’origine. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

