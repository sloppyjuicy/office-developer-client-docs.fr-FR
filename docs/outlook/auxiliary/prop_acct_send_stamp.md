---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Renvoie le accountsendstamp.
ms.openlocfilehash: b86fb4526703802e843f3976655621c4eb676e76
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601148"
---
# <a name="prop_acct_send_stamp"></a>PROP_ACCT_SEND_STAMP

Renvoie le cachet « envoyer » du compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x000E  <br/> |
|Type de propriété :  <br/> |PT_UNICODE  <br/> |
|Balise de propriété :  <br/> |0x000E001F  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Obtenez cette propriété à [l’aide de IOlkAccount::GetProp](iolkaccount-getprop.md). Si le client tente de définir cette propriété, cette propriété renvoie **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

