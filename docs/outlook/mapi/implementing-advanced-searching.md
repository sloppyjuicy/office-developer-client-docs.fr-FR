---
title: Mise en œuvre de la recherche avancée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407388"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="15bdb-103">Mise en œuvre de la recherche avancée</span><span class="sxs-lookup"><span data-stu-id="15bdb-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="15bdb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15bdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15bdb-105">Certains conteneurs de carnet d’adresses peuvent prendre en charge une fonctionnalité de recherche avancée qui permet aux clients d’effectuer des recherches sur des propriétés autres que **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="15bdb-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="15bdb-106">Pour prendre en charge les recherches avancées, votre fournisseur doit implémenter un conteneur spécial accessible via la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de vos autres conteneurs.</span><span class="sxs-lookup"><span data-stu-id="15bdb-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="15bdb-107">**PR_SEARCH** contient un objet conteneur qui donne accès à un tableau d’affichage qui décrit la boîte de dialogue utilisée pour entrer et modifier les critères de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="15bdb-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="15bdb-108">**Pour prendre en charge la recherche avancée**</span><span class="sxs-lookup"><span data-stu-id="15bdb-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="15bdb-109">Définissez une propriété pour chacun de vos critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="15bdb-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="15bdb-110">Dans la section du code de la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de votre conteneur qui gère la propriété **PR_SEARCH:**</span><span class="sxs-lookup"><span data-stu-id="15bdb-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="15bdb-111">Vérifiez que le client demande l’interface **IMAPIContainer.**</span><span class="sxs-lookup"><span data-stu-id="15bdb-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="15bdb-112">Si une interface inappropriée est demandée, échouez et renvoyez MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="15bdb-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="15bdb-113">Créez un objet de recherche qui prend en charge l’interface **IMAPIContainer.**</span><span class="sxs-lookup"><span data-stu-id="15bdb-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="15bdb-114">À ce stade, un appel est effectué à la méthode **IMAPIProp::OpenProperty** de votre conteneur de recherche pour récupérer sa propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="15bdb-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="15bdb-115">Votre fournisseur doit fournir une table d’affichage, généralement via un appel à [BuildDisplayTable](builddisplaytable.md), qui décrit la boîte de dialogue de recherche avancée du conteneur.</span><span class="sxs-lookup"><span data-stu-id="15bdb-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="15bdb-116">MAPI affiche la boîte de dialogue de recherche, ce qui permet à l’utilisateur d’entrer les critères appropriés.</span><span class="sxs-lookup"><span data-stu-id="15bdb-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="15bdb-117">Lorsque l’utilisateur a terminé, MAPI appelle la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) du conteneur pour stocker les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="15bdb-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="15bdb-118">Un appel est effectué pour demander la table des matières de votre conteneur de recherche.</span><span class="sxs-lookup"><span data-stu-id="15bdb-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="15bdb-119">Remplir la table des matières avec toutes les entrées du conteneur qui correspondent aux critères.</span><span class="sxs-lookup"><span data-stu-id="15bdb-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

