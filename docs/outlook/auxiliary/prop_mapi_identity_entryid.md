---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Récupère ou définit l’ID d’entrée du carnet d’adresses pour le compte.
ms.openlocfilehash: 9d926b5b68fb41962946700f585d6a3629aacd25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601134"
---
# <a name="prop_mapi_identity_entryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Récupère ou définit l’ID d’entrée du carnet d’adresses pour le compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x2002  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Balise de propriété :  <br/> |0x20020102  <br/> |
|Accès :  <br/> |Lecture/écriture  <br/> |
   
## <a name="remarks"></a>Remarques

 **PROP \_ MAPI \_ IDENTITY \_ ENTRYID n’est** pas censé exister sur chaque compte. Par exemple, un compte Exchange peut avoir PROP **\_ MAPI \_ IDENTITY \_ ENTRYID** définie et non [PROP \_ ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), tandis que pour un compte SMTP/POP3, la situation est inversée. **PROP \_ MAPI_IDENTITY_ENTRYID** renvoie un ID d’entrée similaire à la valeur renvoyée par  _lppEntryID_ dans [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx). 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

