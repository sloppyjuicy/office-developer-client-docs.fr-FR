---
title: Prise en charge des recherches dans les fournisseurs de magasins de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425385"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="7c9a7-103">Prise en charge des recherches dans les fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="7c9a7-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="7c9a7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c9a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c9a7-105">Les applications clientes ont souvent des composants d’interface utilisateur dédiés à la recherche de messages dans une magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="7c9a7-106">Les critères de recherche sont spécifiés dans l’interface [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) au moyen des méthodes [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) et [IMAPIContainer::GetSearchCriteria.](imapicontainer-getsearchcriteria.md)</span><span class="sxs-lookup"><span data-stu-id="7c9a7-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="7c9a7-107">Les clients utilisent la propriété **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) de l’objet de la boutique de messages pour identifier le dossier racine dans la magasin de messages qui contient des dossiers pour les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="7c9a7-108">Le dossier de résultats de recherche est souvent un dossier au niveau supérieur de la magasin de messages qui ne fait pas partie de l’arborescence des dossiers IPM et qui est donc masqué.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="7c9a7-109">Que votre fournisseur de magasins de messages utilise un dossier de résultats de recherche permanent ou en crée un lorsqu’un client ouvre l’identificateur d’entrée stocké dans la **propriété PR_FINDER_ENTRYID** est un détail d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="7c9a7-110">Il est un peu plus facile pour votre fournisseur de magasin de messages d’utiliser un dossier permanent créé lors de la création de la magasin de messages, car cela évite la complication de la vérification de l’identificateur d’entrée chaque fois qu’un dossier est ouvert pour déterminer s’il faut créer un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="7c9a7-111">Toutefois, tous les fournisseurs de magasins de messages ne peuvent pas le faire . notamment, les banques de messages en lecture seule qui fournissent une interface MAPI à une base de données héritée ne sont souvent pas autorisées ou ne peuvent pas créer un dossier de résultats de recherche permanent dans le mécanisme de stockage sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="7c9a7-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c9a7-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c9a7-112">See also</span></span>



[<span data-ttu-id="7c9a7-113">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="7c9a7-113">Message Store Features</span></span>](message-store-features.md)

