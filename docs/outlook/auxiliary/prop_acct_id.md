---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Renvoie un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.
ms.openlocfilehash: e1a4d5cd6594dc4b85b356d76b1e09c96d863364
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605329"
---
# <a name="prop_acct_id"></a>PROP_ACCT_ID

Renvoie un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0001  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Balise de propriété :  <br/> |0x00010003  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md). Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**. 
  
Cette propriété est différente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) en ce que sa valeur est unique uniquement parmi tous les comptes au sein de ce profil dans lesquels le compte a été créé, tandis que PROP ACCT_MINI_UID identifie de manière unique le compte à l’intérieur et à l’extérieur du profil dans lequel le compte **\_ a** été créé. Lorsqu’un message avec ces propriétés se déplace sur un deuxième ordinateur avec un profil Outlook différent et un ensemble de comptes différent, **PROP_ACCT_ID** peut être en conflit avec un compte dans le profil du deuxième ordinateur, et **PROP_ACCT_MINI_UID** peut identifier de manière unique le compte d’origine dans le profil d’origine. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

