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
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="4e6e3-103">Mappage d’attributs de messagerie Internet sur des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4e6e3-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="4e6e3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e6e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e6e3-105">Cette annexe décrit comment un fournisseur de transport MAPI ou d’une passerelle prenant en charge MAPI qui se connecte à Internet doit traduire entre les propriétés de message MAPI et les attributs de message Simple Mail Transport Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="4e6e3-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="4e6e3-106">SMTP est le protocole de messagerie utilisé sur beaucoup d’Internet.</span><span class="sxs-lookup"><span data-stu-id="4e6e3-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="4e6e3-107">SMTP définit un ensemble d’en-têtes de message, l’enveloppe du message et un format de contenu du message.</span><span class="sxs-lookup"><span data-stu-id="4e6e3-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="4e6e3-108">SMTP est entièrement documentée dans un ensemble de deux documents, la spécification RFC 821 et 822, qui se trouvent à un nombre de sites FTP et les services Web sur Internet.</span><span class="sxs-lookup"><span data-stu-id="4e6e3-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="4e6e3-109">Pour plus d’informations sur le protocole SMTP utilisé pour communiquer avec les agents de messagerie SMTP, voir RFC 821, « Simple Mail Transfer Protocol, » à [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="4e6e3-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="4e6e3-110">Pour les en-têtes de message standard et d’adressage, voir RFC 822, « Standard pour le Format des Messages Internet ARPA texte, » à [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="4e6e3-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="4e6e3-111">MIME, voir RFC 1521, « partie MIME (Multipurpose Internet Mail Extensions) un : mécanismes de spécification et décrivant le Format du corps de Message Internet, « à [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="4e6e3-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="4e6e3-112">L’objectif de mappage des attributs de message SMTP sur des propriétés MAPI (et vice versa) est pour vous assurer que l’intégralité du contenu des messages MAPI, en plus de ce qui peut être codé à l’aide d’attributs de message SMTP natives, peut être échangé entre les différents MAPI fiable composants qui doivent communiquer via Internet.</span><span class="sxs-lookup"><span data-stu-id="4e6e3-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="4e6e3-113">Ce document est basé sur le travail déjà effectué sur ces composants chez Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4e6e3-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="4e6e3-114">Ce document suppose que vous maîtrisez les transports MAPI, TNEF et SMTP mail.</span><span class="sxs-lookup"><span data-stu-id="4e6e3-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="4e6e3-115">Il cherche à être concise plutôt qu’apparaît très clairement.</span><span class="sxs-lookup"><span data-stu-id="4e6e3-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="4e6e3-116">Par convention, « sortant » désigne pour envoyer du courrier lors des déplacements entre un UA compatible MAPI ou les MTA à Internet, et « entrant » le courrier circulant à partir d’Internet à un composant MAPI.</span><span class="sxs-lookup"><span data-stu-id="4e6e3-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

