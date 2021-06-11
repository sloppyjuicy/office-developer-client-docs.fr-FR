---
title: Mappage des attributs de messagerie Internet aux propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355817"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="39d22-103">Mappage des attributs de messagerie Internet aux propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="39d22-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="39d22-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39d22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39d22-105">Cette annexe décrit comment un fournisseur de transport MAPI ou une passerelle MAPI qui se connecte à Internet doit se traduire entre les propriétés de message MAPI et les attributs de message SMTP (Simple Mail Transport Protocol).</span><span class="sxs-lookup"><span data-stu-id="39d22-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="39d22-106">SMTP est le protocole de messagerie utilisé sur une grande partie d’Internet.</span><span class="sxs-lookup"><span data-stu-id="39d22-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="39d22-107">SMTP définit un ensemble d’en-têtes de message (enveloppe de message) et un format de contenu de message.</span><span class="sxs-lookup"><span data-stu-id="39d22-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="39d22-108">SMTP est entièrement documenté dans un ensemble de deux documents, RFC 821 et RFC 822, disponibles sur un certain nombre de sites FTP et WWW sur Internet.</span><span class="sxs-lookup"><span data-stu-id="39d22-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="39d22-109">Pour plus d’informations sur le protocole SMTP utilisé pour communiquer avec des agents de messagerie SMTP, voir RFC 821, « Simple Mail Transfer Protocol », à [https://www.rfc-editor.org](https://www.rfc-editor.org) l’adresse .</span><span class="sxs-lookup"><span data-stu-id="39d22-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="39d22-110">Pour les en-têtes d’adresse et de message standard, voir RFC 822, « Standard for the Format of ARPA Internet Text Messages », à [https://www.rfc-editor.org](https://www.rfc-editor.org) l’adresse .</span><span class="sxs-lookup"><span data-stu-id="39d22-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="39d22-111">Pour MIME, voir RFC 1521, « MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies », à [https://www.rfc-editor.org](https://www.rfc-editor.org) l’adresse .</span><span class="sxs-lookup"><span data-stu-id="39d22-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="39d22-112">L’objectif du mappage des attributs de message SMTP aux propriétés MAPI (et vice versa) est de s’assurer que le contenu complet des messages MAPI, au-delà de celui qui peut être codé à l’aide d’attributs de message SMTP natifs, peut être échangé de manière fiable entre différents composants MAPI qui doivent communiquer sur Internet.</span><span class="sxs-lookup"><span data-stu-id="39d22-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="39d22-113">Ce document est basé sur le travail déjà effectué sur ces composants chez Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39d22-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="39d22-114">Ce document suppose une connaissance des transports MAPI, du TNEF et du courrier SMTP.</span><span class="sxs-lookup"><span data-stu-id="39d22-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="39d22-115">Il s’efforce d’être concis plutôt que d’être clairement clair.</span><span class="sxs-lookup"><span data-stu-id="39d22-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="39d22-116">En tant que convention, « sortant » désigne les messages qui circulent d’une UC ou d’un MTA compatible MAPI vers Internet, et « entrant » désigne les messages qui circulent d’Internet vers un composant MAPI.</span><span class="sxs-lookup"><span data-stu-id="39d22-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

