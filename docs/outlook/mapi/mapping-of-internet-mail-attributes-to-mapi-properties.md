---
title: Mappage des attributs de messagerie Internet aux propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355817"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Mappage des attributs de messagerie Internet aux propriétés MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette annexe décrit comment un fournisseur de transport MAPI ou une passerelle MAPI qui se connecte à Internet doit effectuer une conversion entre les propriétés de message MAPI et les attributs de message SMTP (simple mail transport Protocol). SMTP est le protocole de messagerie utilisé sur une grande partie d'Internet. SMTP définit un ensemble d'en-têtes de message, à savoir l'enveloppe de message et un format de contenu de message. SMTP est entièrement documenté dans un ensemble de deux documents, RFC 821 et RFC 822, qui peuvent être trouvés sur un certain nombre de sites FTP et WWW sur Internet.
  
Pour plus d'informations sur le protocole SMTP utilisé pour communiquer avec des agents de messagerie SMTP, consultez le document RFC 821, «simple Mail Transfer [https://www.rfc-editor.org](https://www.rfc-editor.org)Protocol», à l'adresse.
  
Pour les en-têtes d'adressage et de message standard, consultez la rubrique RFC 822, «Standard for the format of ARPA [https://www.rfc-editor.org](https://www.rfc-editor.org)Internet Text messages» à l'adresse.
  
Pour MIME, reportez-vous à la rubrique RFC 1521, «MIME (Multipurpose Internet Mail Extensions) part one: mécanismes permettant de spécifier et de [https://www.rfc-editor.org](https://www.rfc-editor.org)décrire le format des corps de message Internet» à l'adresse.
  
L'objectif du mappage des attributs de message SMTP aux propriétés MAPI (et inversement) est de s'assurer que le contenu complet des messages MAPI, plus ou plus, qui peuvent être codés à l'aide d'attributs de message SMTP natifs, peut être échangé en toute fiabilité entre différents MAPI composants qui doivent communiquer sur Internet. Ce document est basé sur le travail déjà réalisé sur les composants de ce type chez Microsoft. 
  
Ce document suppose une connaissance des transports MAPI, TNEF et SMTP mail. Elle s'efforce d'être concise et non très claire.
  
En guise de Convention, «sortant» fait référence au courrier circulant à partir d'un agent client ou MTA conforme à la norme MAPI sur Internet, et «entrant» fait référence au courrier circulant depuis Internet vers un composant MAPI.
  

