---
title: Corrélation TNEF dans les passerelles SMTP et des Transports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ec1d826ee2b3b46685a2c03dfaf45d2843869cc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787359"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="dc635-103">Corrélation TNEF dans les passerelles SMTP et des Transports</span><span class="sxs-lookup"><span data-stu-id="dc635-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="dc635-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc635-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc635-105">Systèmes, celles qui utilisent le protocole SMTP, utilisez la valeur de l’en-tête SMTP MessageID et la propriété **PR_TNEF_CORRELATION_KEY** pour implémenter la corrélation TNEF en fonction de passerelles et des transports qui se connectent à internet.</span><span class="sxs-lookup"><span data-stu-id="dc635-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="dc635-106">La valeur de l’en-tête MessageID du message sortant doit être copiée dans la propriété **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) et codée dans l’attribut [attMAPIProps](attmapiprops.md) de l’objet stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="dc635-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="dc635-107">Notez que **PR_TNEF_CORRELATION_KEY** est une propriété binaire, tandis que l’ID du message est une chaîne ; le terminateur null doit être inclus dans la copie et la comparaison.</span><span class="sxs-lookup"><span data-stu-id="dc635-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="dc635-108">Cette technique est utilisée par tous les logiciels Microsoft qui connecte des systèmes de messagerie basé sur MAPI à Internet, telle que Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dc635-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="dc635-109">Cette technique doit être utilisée par les passerelles SMTP et les transports de se connecter aux systèmes qui prennent en charge des clients MAPI afin d’optimiser l’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="dc635-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

