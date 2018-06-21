---
title: Mappage d’attributs de messagerie Internet sur des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4d1bc5fc5a5e304d81ab4252a527d0e52b0d6e3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19784790"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Mappage d’attributs de messagerie Internet sur des propriétés MAPI

  
  
**S’applique à**: Outlook 
  
Cette annexe décrit comment un fournisseur de transport MAPI ou d’une passerelle prenant en charge MAPI qui se connecte à Internet doit traduire entre les propriétés de message MAPI et les attributs de message Simple Mail Transport Protocol (SMTP). SMTP est le protocole de messagerie utilisé sur beaucoup d’Internet. SMTP définit un ensemble d’en-têtes de message, l’enveloppe du message et un format de contenu du message. SMTP est entièrement documentée dans un ensemble de deux documents, la spécification RFC 821 et 822, qui se trouvent à un nombre de sites FTP et les services Web sur Internet.
  
Pour plus d’informations sur le protocole SMTP utilisé pour communiquer avec les agents de messagerie SMTP, voir RFC 821, « Simple Mail Transfer Protocol, » à [http://www.rfc-editor.org](http://www.rfc-editor.org).
  
Pour les en-têtes de message standard et d’adressage, voir RFC 822, « Standard pour le Format des Messages Internet ARPA texte, » à [http://www.rfc-editor.org](http://www.rfc-editor.org).
  
MIME, voir RFC 1521, « partie MIME (Multipurpose Internet Mail Extensions) un : mécanismes de spécification et décrivant le Format du corps de Message Internet, « à [http://www.rfc-editor.org](http://www.rfc-editor.org).
  
L’objectif de mappage des attributs de message SMTP sur des propriétés MAPI (et vice versa) est pour vous assurer que l’intégralité du contenu des messages MAPI, en plus de ce qui peut être codé à l’aide d’attributs de message SMTP natives, peut être échangé entre les différents MAPI fiable composants qui doivent communiquer via Internet. Ce document est basé sur le travail déjà effectué sur ces composants chez Microsoft. 
  
Ce document suppose que vous maîtrisez les transports MAPI, TNEF et SMTP mail. Il cherche à être concise plutôt qu’apparaît très clairement.
  
Par convention, « sortant » désigne pour envoyer du courrier lors des déplacements entre un UA compatible MAPI ou les MTA à Internet, et « entrant » le courrier circulant à partir d’Internet à un composant MAPI.
  

