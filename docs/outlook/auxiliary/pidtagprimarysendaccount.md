---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Spécifie l’endstamp de compte principal pour un message.
ms.openlocfilehash: b4d0188d75cdf03a78c198377c03a885fce3654b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601232"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

Spécifie le cachet « envoyer » du compte principal pour un message.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Identificateur :  <br/> |0x0E28  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Compte  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété s’applique à un objet message MAPI. Pour un message reçu, le cachet « envoyer » du compte principal indique avec quel compte un avant ou une réponse doit être envoyé. Pour un message sortant, il détermine le compte avec lequel envoyer le message. Sa valeur est la [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) de l’interface [IOlkAccount](iolkaccount.md) du compte avec lequel le message est envoyé. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
- [Propriétés MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [Propriété canonique PidTagPrimarySendAccount](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

