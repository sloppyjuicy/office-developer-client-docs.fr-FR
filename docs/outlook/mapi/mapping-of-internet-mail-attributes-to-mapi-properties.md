---
title: Mappage des attributs de messagerie Internet aux propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
ms.openlocfilehash: 33458b499f837ff98c6c438fc357357ad54dc075
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374067"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Mappage des attributs de messagerie Internet aux propriétés MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette annexe décrit comment un fournisseur de transport MAPI ou une passerelle MAPI qui se connecte à Internet doit se traduire entre les propriétés de message MAPI et les attributs de message SMTP (Simple Mail Transport Protocol). SMTP est le protocole de messagerie utilisé sur une grande partie d’Internet. SMTP définit un ensemble d’en-têtes de message (enveloppe de message) et un format de contenu de message. SMTP est entièrement documenté dans un ensemble de deux documents, RFC 821 et RFC 822, disponibles sur plusieurs sites FTP et WWW sur Internet.
  
Pour plus d’informations sur le protocole SMTP utilisé pour communiquer avec des agents de messagerie SMTP, voir RFC 821, « Simple Mail Transfer Protocol », à l’adresse [https://www.rfc-editor.org](https://www.rfc-editor.org).
  
Pour les en-têtes d’adresse et de message standard, voir RFC 822, « Standard for the Format of ARPA Internet Text Messages », à l’adresse [https://www.rfc-editor.org](https://www.rfc-editor.org).
  
Pour MIME, voir RFC 1521, « MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies », à [https://www.rfc-editor.org](https://www.rfc-editor.org)l’adresse .
  
L’objectif du mappage des attributs de message SMTP aux propriétés MAPI (et vice versa) est de s’assurer que le contenu complet des messages MAPI, au-delà de celui qui peut être codé à l’aide d’attributs de message SMTP natifs, peut être échangé de manière fiable entre différents composants MAPI qui doivent communiquer sur Internet. Ce document est basé sur le travail déjà effectué sur ces composants chez Microsoft. 
  
Ce document suppose une connaissance des transports MAPI, du TNEF et du courrier SMTP. Il s’efforce d’être concis plutôt que d’être clairement clair.
  
En tant que convention, « sortant » fait référence au courrier circulant d’une UC ou d’un MTA compatible MAPI vers Internet, et « entrant » désigne le courrier qui se déplace d’Internet vers un composant MAPI.
  

