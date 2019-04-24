---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Spécifie l'adresse de messagerie du compte.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326529"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Spécifie l'adresse de messagerie du compte.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificateur :  <br/> |0x000C  <br/> |
|Type de propriété:  <br/> |PT_UNICODE  <br/> |
|Balise de propriété:  <br/> |0x000C001F  <br/> |
|Access  <br/> |En lecture-écriture.  <br/> |
   
## <a name="remarks"></a>Remarques

 **PROP_ACCT_USER_EMAIL_ADDR** n'est pas censé exister sur chaque compte. Par exemple, un compte Exchange peut avoir [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) mais pas **PROP_ACCT_USER_EMAIL_ADDR**, tandis que pour un compte SMTP/POP3, la situation est inversée.
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)

