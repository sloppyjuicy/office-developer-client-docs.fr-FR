---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: Cette valeur a la valeur True si le compte est Exchange client.
ms.openlocfilehash: 67562acbb7ee5c29948d9e2dd7bfdbf9a7623135
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631166"
---
# <a name="prop_acct_is_exch"></a>PROP_ACCT_IS_EXCH

Cette valeur a la valeur True si le compte est Exchange client.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x0014  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Balise de propriété :  <br/> |0x00140003  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md). Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

