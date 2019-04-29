---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Renvoie un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407164"
---
# <a name="propacctid"></a>PROP_ACCT_ID

Renvoie un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0001  <br/> |
|Type de propriété:  <br/> |PT_LONG  <br/> |
|Balise de propriété:  <br/> |0x00010003  <br/> |
|Access  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à l'aide de [IOlkAccount:: getprop](iolkaccount-getprop.md). Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**. 
  
Cette propriété est différente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) en ce sens que sa valeur n'est unique que pour tous les comptes de ce profil dans lequel le compte a été créé, tandis que **prop\_ACCT_MINI_UID** identifie de manière unique le compte au sein de et en dehors du profil dans lequel le compte a été créé. Lorsqu'un message avec ces propriétés se déplace sur un deuxième ordinateur avec un profil Outlook différent et un autre ensemble de comptes, **PROP_ACCT_ID** peut éventuellement entrer en conflit avec un compte dans le profil du deuxième ordinateur et **PROP_ACCT_MINI_UID** peut identifier de manière unique le compte d'origine dans le profil d'origine. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

