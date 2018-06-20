---
title: Corrélation TNEF dans les passerelles X.400 et des Transports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ea5ca41ef21c72377ade72370e0aee1b313c92d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787356"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="7ab29-103">Corrélation TNEF dans les passerelles X.400 et des Transports</span><span class="sxs-lookup"><span data-stu-id="7ab29-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="7ab29-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ab29-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ab29-105">Passerelles et des transports qui se connectent aux systèmes X.400, utilisez la valeur de l’attribut IM_THIS_IPM X.400 et l’attribut TNEF **attMessageID** pour implémenter la corrélation TNEF.</span><span class="sxs-lookup"><span data-stu-id="7ab29-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="7ab29-106">La valeur de l’attribut IM_THIS_IPM du message sortant est copiée dans **attMessageID** dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="7ab29-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="7ab29-107">L’attribut IM_THIS_IPM X.400 est généralement une chaîne, tandis que l’attribut TNEF **attMessageID** est une chaîne de chiffres hexadécimaux représentant une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="7ab29-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="7ab29-108">Par conséquent, chaque caractère dans l’attribut IM_THIS_IPM X.400, y compris le caractère null de fin doit être converti en une chaîne hexadécimale 2 caractères représentant la valeur de ce caractère ASCII.</span><span class="sxs-lookup"><span data-stu-id="7ab29-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="7ab29-109">Par exemple, si l’attribut IM_THIS_IPM X.400 est la chaîne suivante :</span><span class="sxs-lookup"><span data-stu-id="7ab29-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="7ab29-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="7ab29-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="7ab29-111">la valeur de **attMessageID** est la séquence de chiffres hexadécimaux suivante :</span><span class="sxs-lookup"><span data-stu-id="7ab29-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="7ab29-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="7ab29-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="7ab29-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="7ab29-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="7ab29-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="7ab29-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="7ab29-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="7ab29-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="7ab29-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="7ab29-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="7ab29-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="7ab29-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="7ab29-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="7ab29-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="7ab29-119">Cette technique est utilisée par le connecteur X.400 de Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7ab29-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="7ab29-120">Cette technique doit être utilisée par les passerelles X.400 et les transports de se connecter à Microsoft Exchange Server afin d’optimiser l’interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="7ab29-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="7ab29-121">Pour assurer la compatibilité avec les logiciels Microsoft futures ainsi que présente plus grande, l’attribut IM_THIS_IPM X.400 doit également être copié à la propriété **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7ab29-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="7ab29-122">Toutefois, étant donné que **PR_TNEF_CORRELATION_KEY** est une propriété binaire, aucune conversion en une chaîne hexadécimale n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7ab29-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

