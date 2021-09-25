---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Renvoie un identificateur de compte unique dans Outlook profils.
ms.openlocfilehash: bcfede8ad2716bd09ec1abd3420b7e61777f4a0a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625629"
---
# <a name="prop_acct_mini_uid"></a>PROP_ACCT_MINI_UID

Renvoie un identificateur de compte unique dans Outlook profils.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0003  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Balise de propriété :  <br/> |0x00030003  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md). Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**. 
  
Cette propriété est différente de [PROP_ACCT_ID](prop_acct_id.md) en ce que sa valeur identifie de manière unique le compte à l’intérieur et à l’extérieur du profil dans lequel le compte a été créé, tandis que PROP_ACCT_ID est unique uniquement parmi tous les comptes au sein de ce profil dans lequel le compte **a** été créé. Lorsqu’un message avec ces propriétés se déplace sur un deuxième ordinateur avec un profil Outlook différent et un ensemble de comptes différent, **PROP_ACCT_MINI_UID** peut identifier de manière unique le compte d’origine dans le profil d’origine. Toutefois, **PROP_ACCT_ID** peut être en conflit avec un compte dans le profil du deuxième ordinateur. 
  
## <a name="see-also"></a>Voir aussi

- [PROP_ACCT_ID](prop_acct_id.md)  
- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

