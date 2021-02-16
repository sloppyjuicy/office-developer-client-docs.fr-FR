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
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432260"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="a158b-103">Obtention et définition de plusieurs propriétés</span><span class="sxs-lookup"><span data-stu-id="a158b-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="a158b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a158b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a158b-105">En obtenant et en fixant autant de propriétés que possible avec le moins d’appels possible, l’activité à distance est réduite et la surcharge impliquée dans chaque propriété est réduite.</span><span class="sxs-lookup"><span data-stu-id="a158b-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="a158b-106">Bien que les fournisseurs de services tentent de collecter des propriétés avant d’effectuer un appel de procédure distante pour la récupération ou la modification, vous pouvez optimiser cet effort en demandant plusieurs propriétés pour commencer.</span><span class="sxs-lookup"><span data-stu-id="a158b-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="a158b-107">Par exemple, si vous travaillez avec des listes de routage qui décrivent les destinataires futurs avec des propriétés nommées appartenant à des jeux de propriétés particuliers, traitez tous les destinataires avec deux appels.</span><span class="sxs-lookup"><span data-stu-id="a158b-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="a158b-108">Utilisez un appel à [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour récupérer les identificateurs de toutes les propriétés du destinataire et l’autre appel à [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a158b-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="a158b-109">L’alternative, appeler **GetIDsFromNames** suivi d’un appel à **GetProps** pour chaque destinataire, est beaucoup moins efficace.</span><span class="sxs-lookup"><span data-stu-id="a158b-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

