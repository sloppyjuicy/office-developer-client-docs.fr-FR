---
title: Prise en charge des recherches dans les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f206623103f810b2868502aea7c6804cd306f022
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573193"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="0f68d-103">Prise en charge des recherches dans les fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="0f68d-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="0f68d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f68d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f68d-105">Les applications clientes ont fréquemment certains composants d’interface utilisateur consacrées à la recherche de messages dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="0f68d-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="0f68d-106">Critères de recherche sont spécifiés dans le [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface via les méthodes [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) et [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) .</span><span class="sxs-lookup"><span data-stu-id="0f68d-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="0f68d-107">Clients utilisent la propriété **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) de l’objet de banque de message pour identifier le dossier racine dans le magasin de message qui contient les dossiers de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="0f68d-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="0f68d-108">Le dossier de résultats de recherche est souvent un dossier au niveau supérieur de la banque de messages qui ne fait pas partie de l’arborescence de dossiers IPM et, par conséquent, masqué.</span><span class="sxs-lookup"><span data-stu-id="0f68d-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="0f68d-109">Si votre fournisseur de magasin de message utilise un dossier de résultats de recherche permanente ou crée un lorsqu’un client ouvre l’identificateur d’entrée stockée dans la propriété **PR_FINDER_ENTRYID** est un détail d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="0f68d-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="0f68d-110">Il est un peu plus facile de votre fournisseur de magasin de message à utiliser un dossier permanent qui est créé lors de la création de la banque de messages, car cela évite la complication de vérification de l’identificateur d’entrée à chaque ouverture d’un dossier pour voir s’il faut créer un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="0f68d-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="0f68d-111">Toutefois, tous les fournisseurs de banque de message peuvent faire. en particulier, banques de message en lecture seule ou qui fournissent une interface MAPI pour une base de données hérité souvent ne sont pas autorisés ou ne parvenez pas à créer un dossier de résultats de recherche permanente dans le mécanisme de stockage sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0f68d-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f68d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f68d-112">See also</span></span>



[<span data-ttu-id="0f68d-113">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="0f68d-113">Message Store Features</span></span>](message-store-features.md)

