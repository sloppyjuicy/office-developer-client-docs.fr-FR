---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Récupère ou définit l'ID d'entrée de carnet d'adresses pour le compte.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326431"
---
# <a name="propmapiidentityentryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Récupère ou définit l'ID d'entrée de carnet d'adresses pour le compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x2002  <br/> |
|Type de propriété:  <br/> |PT_BINARY  <br/> |
|Balise de propriété:  <br/> |0x20020102  <br/> |
|Access  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

 **La\_propriété\_EntryID\_MAPI Identity** n'est pas censée exister sur chaque compte. Par exemple, un compte Exchange peut avoir un paramètre **EntryID\_d'identité\_\_MAPI** et pas [prop\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), tandis que pour un compte SMTP/POP3 la situation est inversée. **PROP\_MAPI_IDENTITY_ENTRYID** renvoie un ID d'entrée semblable à la valeur renvoyée par _lppEntryID_ dans [IMAPISession:: QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx). 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

