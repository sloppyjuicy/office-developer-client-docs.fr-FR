---
title: Obtention et définition de plusieurs propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 88c3e0bdb3cc6660e35faf62c5bb63ec2f6352bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590371"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="f84a5-103">Obtention et définition de plusieurs propriétés</span><span class="sxs-lookup"><span data-stu-id="f84a5-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="f84a5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f84a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f84a5-105">En définissant les propriétés autant que possible avec le moins de nombre d’appels, à distance activité est diminuée et de réduire la surcharge due avec chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="f84a5-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="f84a5-106">Bien que les fournisseurs de services tentez de récupérer les propriétés avant d’effectuer un appel de procédure distante pour l’extraction ou de modification, vous pouvez optimiser cette initiative en demandant plusieurs propriétés pour commencer.</span><span class="sxs-lookup"><span data-stu-id="f84a5-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="f84a5-107">Par exemple, si vous travaillez avec des listes de routage qui décrivent les destinataires futurs avec des propriétés nommées appartenant à des jeux de propriétés particulière, traiter tous les destinataires avec deux appels.</span><span class="sxs-lookup"><span data-stu-id="f84a5-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="f84a5-108">Utilisez un appel à [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour récupérer les identificateurs de toutes les propriétés du destinataire et l’autre [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f84a5-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="f84a5-109">L’alternative, un appel à **GetIDsFromNames** suivi par un appel à **GetProps** pour chaque destinataire, est beaucoup plus efficace.</span><span class="sxs-lookup"><span data-stu-id="f84a5-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

