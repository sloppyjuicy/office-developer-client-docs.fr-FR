---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Renvoie un identificateur de compte qui est unique dans les profils Outlook.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327628"
---
# <a name="propacctminiuid"></a>PROP_ACCT_MINI_UID

Renvoie un identificateur de compte qui est unique dans les profils Outlook.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0003  <br/> |
|Type de propriété:  <br/> |PT_LONG  <br/> |
|Balise de propriété:  <br/> |0x00030003  <br/> |
|Access  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md). Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**. 
  
Cette propriété est différente de [PROP_ACCT_ID](prop_acct_id.md) en ce sens qu'elle identifie de manière unique le compte à l'intérieur et à l'extérieur du profil dans lequel le compte a été créé, tandis que **PROP_ACCT_ID** n'est unique que pour tous les comptes se trouvant dans ce profil. dans lequel le compte a été créé. Lorsqu'un message avec ces propriétés se déplace sur un deuxième ordinateur avec un profil Outlook différent et un autre ensemble de comptes, **PROP_ACCT_MINI_UID** peut identifier de manière unique le compte d'origine dans le profil d'origine. Toutefois, les **PROP_ACCT_ID** peuvent éventuellement entrer en conflit avec un compte dans le profil du deuxième ordinateur. 
  
## <a name="see-also"></a>Voir aussi

- [PROP_ACCT_ID](prop_acct_id.md)  
- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

