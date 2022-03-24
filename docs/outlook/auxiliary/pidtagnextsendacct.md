---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Spécifie l’endstamp de compte secondaire pour le message.
ms.openlocfilehash: 3e41fc03f70cb26c01d7664c5844be367dba42eb
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63716396"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Spécifie le cachet « envoyer » du compte secondaire pour le message.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Identificateur :  <br/> |0x0E29  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Outlook application  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété s’applique à un objet message MAPI. Pour un message reçu, le cachet « envoyer » du compte secondaire indique avec quel compte un avant ou une réponse doit être envoyé, si le forward ou la réponse ne peut pas être envoyé avec le compte principal. Pour un message sortant, le cachet « envoyer » du compte secondaire détermine avec quel compte envoyer le message, si le message ne peut pas être envoyé avec le compte principal. Sa valeur est la [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) de l’interface [IOlkAccount](iolkaccount.md) du compte avec lequel le message est envoyé. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
- [Propriétés MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [Propriété canonique PidTagNextSendAcct](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

