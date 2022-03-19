---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Spécifie l’adresse e-mail du compte.
ms.openlocfilehash: 2404c13ae293276b64ea3c6f6e0367137b52f564
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628605"
---
# <a name="prop_acct_user_email_addr"></a>PROP_ACCT_USER_EMAIL_ADDR

Spécifie l’adresse e-mail du compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Identificateur :  <br/> |0x000C  <br/> |
|Type de propriété :  <br/> |PT_UNICODE  <br/> |
|Balise de propriété :  <br/> |0x000C001F  <br/> |
|Accès :  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

 **PROP_ACCT_USER_EMAIL_ADDR** n’est pas censé exister sur chaque compte. Par exemple, un compte Exchange peut avoir des PROP_MAPI_IDENTITY_ENTRYID mais [](prop_mapi_identity_entryid.md) pas **PROP_ACCT_USER_EMAIL_ADDR, alors** que pour un compte SMTP/POP3, la situation est inversée.
  
## <a name="see-also"></a>Consultez aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

