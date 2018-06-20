---
title: Envoi de Messages avec TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e2df265-b9dd-4e19-8ca5-3e31804e9120
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fb26d854b47894d8f37763b17e5ba0b26fd25ff6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787129"
---
# <a name="sending-messages-with-tnef"></a>Envoi de Messages avec TNEF

  
  
**S’applique à**: Outlook 
  
De nombreux fournisseurs de transport envoyer automatiquement tous les messages sortants avec la Neutral Encapsulation Format TNEF (Transport). Le format TNEF est utilisé pour transmettre le texte mis en forme qui prennent en charge les clients et les fournisseurs de banque de messages dans leurs messages, les pièces jointes de différents types et des propriétés personnalisées pour les classes de message personnalisées. Bien que le mode par défaut pour la plupart des fournisseurs de transport consiste à envoyer des messages sortants avec TNEF, certains fournisseurs de transport ne le permettent pas. L’absence de prise en charge pour le format TNEF n’est pas un problème pour les clients de messagerie standards qui envoient et reçoivent des messages IPM. Toutefois, pour les clients basés sur les formulaires ou les clients qui requièrent des propriétés personnalisées, l’utilisation du format TNEF est essentielle. Les concepteurs de clients qui reposent sur des formulaires ou des propriétés personnalisées doivent prendre en charge des fonctionnalités des fournisseurs de transport qu’ils utilisent.
  
Destinataires du message peuvent contrôler ou non un fournisseur de transport transmet les messages avec TNEF en définissant la propriété **PR_SEND_RICH_INFO** . Pour plus d’informations, voir **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Lorsque la propriété **PR_SEND_RICH_INFO** d’un destinataire est définie sur TRUE, un fournisseur de transport qui prend en charge TNEF transmet le message. Lorsque la propriété est définie sur FALSE, la mise en forme est ignoré. Lorsque **PR_SEND_RICH_INFO** n’existe pas, il est le fournisseur de transport pour choisir un plan par défaut d’action. 
  
Lorsque les clients et les fournisseurs de services de créent un destinataire personnalisé, elles peuvent affecter la valeur de sa propriété **PR_SEND_RICH_INFO** en transmettant l’indicateur MAPI_SEND_NO_RICH_INFO dans le paramètre _ulFlags_ au **IAddrBook::CreateOneOff** ou ** IMAPISupport::CreateOneOff** d’appel. Pour plus d’informations, voir [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) et [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Le passage de MAPI_SEND_NO_RICH_INFO entraîne MAPI définir la propriété **PR_SEND_RICH_INFO** de destinataire personnalisé sur FALSE. dans la plupart des cas ne pas en passant l’indicateur entraîne MAPI définir la propriété sur TRUE. La seule exception est si l’adresse du destinataire personnalisé est interprétée comme une adresse Internet. Dans ce une cas, MAPI définit **PR_SEND_RICH_INFO** sur FALSE. 
  

