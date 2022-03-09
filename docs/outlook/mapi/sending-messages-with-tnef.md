---
title: Envoi de messages avec TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
ms.openlocfilehash: 260e3a229809502cc5f8bff086934d3aee339544
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380696"
---
# <a name="sending-messages-with-tnef"></a>Envoi de messages avec TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreux fournisseurs de transport envoient automatiquement tous les messages sortants avec le format TNEF (Transport Neutral Encapsulation Format). Le format TNEF permet de transmettre le texte formaté que de nombreux clients et fournisseurs de magasins de messages peuvent prendre en charge dans leurs messages, pièces jointes de différents types et propriétés personnalisées pour les classes de messages personnalisées. Bien que le mode par défaut pour la plupart des fournisseurs de transport consiste à envoyer des messages sortants avec TNEF, certains fournisseurs de transport ne le supportent pas. Le manque de prise en charge du TNEF n’est pas un problème pour les clients de messagerie standard qui envoient et reçoivent des messages IPM. Toutefois, pour les clients basés sur un formulaire ou les clients qui nécessitent des propriétés personnalisées, l’utilisation de TNEF est essentielle. Les concepteurs de clients qui s’appuient sur des formulaires ou des propriétés personnalisées doivent connaître les fonctionnalités des fournisseurs de transport qu’ils utilisent.
  
Les destinataires du message peuvent contrôler si un fournisseur de transport transmet ou non des messages avec TNEF en **PR_SEND_RICH_INFO propriété.** Pour plus d’informations, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Lorsque la propriété **PR_SEND_RICH_INFO d’un** destinataire est définie sur TRUE, un fournisseur de transport qui prend en charge le TNEF la transmet avec le message. Lorsque la propriété est définie sur FALSE, la mise en forme est ignorée. Lorsque **PR_SEND_RICH_INFO** n’existe pas, c’est au fournisseur de transport de choisir une ligne de route par défaut. 
  
Lorsque les clients et les fournisseurs de services créent un destinataire personnalisé, ils peuvent affecter la valeur de sa propriété **PR_SEND_RICH_INFO** en passant l’indicateur MAPI_SEND_NO_RICH_INFO dans le paramètre _ulFlags_ à l’appel **IAddrBook::CreateOneOff** ou **IMAPISupport::CreateOneOff** . Pour plus d’informations, voir [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) and [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Le MAPI_SEND_NO_RICH_INFO entraîne mapI à définir la propriété de **PR_SEND_RICH_INFO du destinataire** personnalisé sur FALSE ; dans la plupart des cas, si l’indicateur n’est pas passé, MAPI lui donne la valeur TRUE. La seule exception est si l’adresse du destinataire personnalisé est interprétée comme une adresse Internet. Dans ce cas, MAPI **définit PR_SEND_RICH_INFO** sur FALSE. 
  

