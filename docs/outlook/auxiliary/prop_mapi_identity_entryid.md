---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Récupère ou définit l’ID d’entrée de carnet d’adresses pour le compte.
ms.openlocfilehash: d85a779da36c2780fe058f906086f61cfc47d5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782814"
---
# <a name="propmapiidentityentryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Récupère ou définit l’ID d’entrée de carnet d’adresses pour le compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0 x 2002  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x20020102  <br/> |
|Access :  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

 **Propriétés\_MAPI\_identité\_ENTRYID** n’est pas censé exister sur chaque compte. Par exemple, un compte Exchange peut avoir **propriétés\_MAPI\_identité\_ENTRYID** définir et pas [propriétés\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), tandis que d’un compte SMTP/POP3 la situation est inversée. **PROPRIÉTÉS\_MAPI_IDENTITY_ENTRYID** renvoie un identificateur d’entrée est similaire à la valeur renvoyée par _lppEntryID_ dans [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx). 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

