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
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="861d9-103">Mappage des attributs de messagerie Internet aux propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="861d9-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="861d9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="861d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="861d9-105">Cette annexe décrit comment un fournisseur de transport MAPI ou une passerelle MAPI qui se connecte à Internet doit effectuer une conversion entre les propriétés de message MAPI et les attributs de message SMTP (simple mail transport Protocol).</span><span class="sxs-lookup"><span data-stu-id="861d9-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="861d9-106">SMTP est le protocole de messagerie utilisé sur une grande partie d'Internet.</span><span class="sxs-lookup"><span data-stu-id="861d9-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="861d9-107">SMTP définit un ensemble d'en-têtes de message, à savoir l'enveloppe de message et un format de contenu de message.</span><span class="sxs-lookup"><span data-stu-id="861d9-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="861d9-108">SMTP est entièrement documenté dans un ensemble de deux documents, RFC 821 et RFC 822, qui peuvent être trouvés sur un certain nombre de sites FTP et WWW sur Internet.</span><span class="sxs-lookup"><span data-stu-id="861d9-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="861d9-109">Pour plus d'informations sur le protocole SMTP utilisé pour communiquer avec des agents de messagerie SMTP, consultez le document RFC 821, «simple Mail Transfer [https://www.rfc-editor.org](https://www.rfc-editor.org)Protocol», à l'adresse.</span><span class="sxs-lookup"><span data-stu-id="861d9-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="861d9-110">Pour les en-têtes d'adressage et de message standard, consultez la rubrique RFC 822, «Standard for the format of ARPA [https://www.rfc-editor.org](https://www.rfc-editor.org)Internet Text messages» à l'adresse.</span><span class="sxs-lookup"><span data-stu-id="861d9-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="861d9-111">Pour MIME, reportez-vous à la rubrique RFC 1521, «MIME (Multipurpose Internet Mail Extensions) part one: mécanismes permettant de spécifier et de [https://www.rfc-editor.org](https://www.rfc-editor.org)décrire le format des corps de message Internet» à l'adresse.</span><span class="sxs-lookup"><span data-stu-id="861d9-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="861d9-112">L'objectif du mappage des attributs de message SMTP aux propriétés MAPI (et inversement) est de s'assurer que le contenu complet des messages MAPI, plus ou plus, qui peuvent être codés à l'aide d'attributs de message SMTP natifs, peut être échangé en toute fiabilité entre différents MAPI composants qui doivent communiquer sur Internet.</span><span class="sxs-lookup"><span data-stu-id="861d9-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="861d9-113">Ce document est basé sur le travail déjà réalisé sur les composants de ce type chez Microsoft.</span><span class="sxs-lookup"><span data-stu-id="861d9-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="861d9-114">Ce document suppose une connaissance des transports MAPI, TNEF et SMTP mail.</span><span class="sxs-lookup"><span data-stu-id="861d9-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="861d9-115">Elle s'efforce d'être concise et non très claire.</span><span class="sxs-lookup"><span data-stu-id="861d9-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="861d9-116">En guise de Convention, «sortant» fait référence au courrier circulant à partir d'un agent client ou MTA conforme à la norme MAPI sur Internet, et «entrant» fait référence au courrier circulant depuis Internet vers un composant MAPI.</span><span class="sxs-lookup"><span data-stu-id="861d9-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

