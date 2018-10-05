---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Spécifie l’accountsendstamp secondaire pour le message.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396476"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Indique le compte secondaire « Envoyer » pour le message.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Identificateur :  <br/> |0x0E29  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété s’applique à un objet de message MAPI. Pour un message reçu, l’horodatage « envoyer » de compte secondaire indique quel compte de transfert ou une réponse doit être envoyée, si le transfert et réponse ne peut pas être envoyé avec le compte principal. Pour un message sortant, le compte secondaire « Envoyer » horodatage détermine avec le compte à envoyer le message, si le message ne peut pas être envoyé avec le compte principal. Sa valeur est la valeur [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) à partir de l’interface [IOlkAccount](iolkaccount.md) du compte avec lequel le message est envoyé. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
- [Propriétés MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [Propriété canonique PidTagNextSendAcct](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

