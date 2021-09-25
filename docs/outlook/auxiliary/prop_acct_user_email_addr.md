---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Spécifie l’adresse e-mail du compte.
ms.openlocfilehash: 3115098fab145194f4a2bb1333e4dd625dfc55c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557063"
---
# <a name="prop_acct_user_email_addr"></a>PROP_ACCT_USER_EMAIL_ADDR

Spécifie l’adresse e-mail du compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x000C  <br/> |
|Type de propriété :  <br/> |PT_UNICODE  <br/> |
|Balise de propriété :  <br/> |0x000C001F  <br/> |
|Accès :  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

 **PROP_ACCT_USER_EMAIL_ADDR** n’est pas censé exister sur chaque compte. Par exemple, un compte Exchange [](prop_mapi_identity_entryid.md) peut avoir des PROP_MAPI_IDENTITY_ENTRYID mais pas PROP_ACCT_USER_EMAIL_ADDR **,** alors que pour un compte SMTP/POP3, la situation est inversée.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

