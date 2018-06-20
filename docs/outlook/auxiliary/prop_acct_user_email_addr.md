---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Spécifie l’adresse de messagerie pour le compte.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782817"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Spécifie l’adresse de messagerie pour le compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x000C  <br/> |
|Type de propriété :  <br/> |PT_UNICODE  <br/> |
|Balise de propriété :  <br/> |0x000C001F  <br/> |
|Access :  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

 **PROP_ACCT_USER_EMAIL_ADDR** n’est pas censé exister sur chaque compte. Par exemple, un compte Exchange peut avoir [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) mais pas **PROP_ACCT_USER_EMAIL_ADDR**, tandis que pour un compte SMTP/POP3, la situation est inversée.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

