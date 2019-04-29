---
title: Envoi de messages avec TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7ff7f79b5e74412e9bbb4b4882c6a7d45e50fe6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420849"
---
# <a name="sending-messages-with-tnef"></a>Envoi de messages avec TNEF

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreux fournisseurs de transport envoient automatiquement tous les messages sortants avec le format TNEF (Transport Neutral Encapsulation Format). Le format TNEF est utilisé pour transmettre le texte mis en forme que de nombreux clients et fournisseurs de banques de messages prennent en charge dans leurs messages, les pièces jointes de différents types et les propriétés personnalisées pour les classes de message personnalisées. Bien que le mode par défaut pour la plupart des fournisseurs de transport consiste à envoyer des messages sortants avec TNEF, certains fournisseurs de transport ne le prennent pas en charge. Le manque de prise en charge de TNEF n'est pas un problème pour les clients de messagerie standard qui envoient et reçoivent des messages IPM. Toutefois, pour les clients basés sur des formulaires ou les clients qui nécessitent des propriétés personnalisées, l'utilisation du format TNEF est essentielle. Les concepteurs de clients qui s'appuient sur des formulaires ou des propriétés personnalisées doivent être conscients des capacités des fournisseurs de transport qu'ils utilisent.
  
Les destinataires du message peuvent contrôler si un fournisseur de transport transmet ou non des messages avec TNEF en définissant la propriété **PR_SEND_RICH_INFO** . Pour plus d'informations, voir **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Lorsque la propriété **PR_SEND_RICH_INFO** d'un destinataire est définie sur true, un fournisseur de transport qui prend en charge le format TNEF le transmet avec le message. Lorsque la propriété a la valeur FALSe, la mise en forme est ignorée. Lorsque **PR_SEND_RICH_INFO** n'existe pas, il revient au fournisseur de transport de choisir une action par défaut. 
  
Lorsque les clients et fournisseurs de services créent un destinataire personnalisé, ils peuvent affecter la valeur de sa propriété **PR_SEND_RICH_INFO** en transmettant l'indicateur MAPI_SEND_NO_RICH_INFO dans le paramètre _UlFlags_ à l' **IAddrBook:: CreateOneOff** ou ** Appel de IMAPISupport:: CreateOneOff** . Pour plus d'informations, voir [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) et [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md). En passant MAPI_SEND_NO_RICH_INFO, MAPI affecte la valeur FALSe à la propriété **PR_SEND_RICH_INFO** du destinataire personnalisé; dans la plupart des cas, si l'indicateur n'est pas passé, MAPI affecte à la propriété la valeur TRUE. La seule exception est si l'adresse du destinataire personnalisé est interprétée comme une adresse Internet. Dans ce cas, MAPI définit **PR_SEND_RICH_INFO** sur false. 
  

