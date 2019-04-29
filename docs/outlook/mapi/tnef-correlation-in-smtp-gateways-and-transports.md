---
title: Corrélation TNEF dans les transports et passerelles SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413667"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="d6e3b-103">Corrélation TNEF dans les transports et passerelles SMTP</span><span class="sxs-lookup"><span data-stu-id="d6e3b-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="d6e3b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6e3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6e3b-105">Les passerelles et les transports qui se connectent à des systèmes Internet, ceux qui utilisent le protocole SMTP, utilisent la valeur de l'en-tête SMTP MessageID et la propriété **PR_TNEF_CORRELATION_KEY** pour implémenter la corrélation TNEF.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="d6e3b-106">La valeur de l'en-tête MessageID du message sortant doit être copiée dans la propriété **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) et codée dans l'attribut [attMAPIProps](attmapiprops.md) du flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="d6e3b-107">Notez que **PR_TNEF_CORRELATION_KEY** est une propriété binaire, tandis que le MessageID est une chaîne; la marque de fin null doit être incluse dans la copie et dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="d6e3b-108">Cette technique est utilisée par tous les logiciels Microsoft qui connectent les systèmes de messagerie MAPI à Internet, comme Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="d6e3b-109">Cette technique doit être utilisée par les passerelles et les transports SMTP qui se connectent aux systèmes qui prennent en charge les clients MAPI afin d'optimiser l'interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

