---
title: L’implémentation de recherche avancée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4430b52b470b89bd7d81922b98b121b3a455768f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784173"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="a61ee-103">L’implémentation de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="a61ee-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="a61ee-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a61ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a61ee-105">Certains conteneurs de carnet d’adresses prend en charge une fonction de recherche avancée qui permet aux clients d’effectuer une recherche sur les propriétés de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a61ee-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="a61ee-106">Pour prendre en charge les recherches avancées, votre fournisseur doit implémenter un conteneur spécial qui est accessible via la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de vos autres conteneurs.</span><span class="sxs-lookup"><span data-stu-id="a61ee-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="a61ee-107">**PR_SEARCH** contient un objet conteneur qui fournit l’accès à un tableau d’affichage qui décrit la boîte de dialogue permet d’entrer et de modifier les critères de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="a61ee-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="a61ee-108">**Pour prendre en charge les recherche avancée**</span><span class="sxs-lookup"><span data-stu-id="a61ee-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="a61ee-109">Définir une propriété pour chacun de vos critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="a61ee-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="a61ee-110">Dans la section de code de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) méthode votre conteneur qui gère la propriété **PR_SEARCH** :</span><span class="sxs-lookup"><span data-stu-id="a61ee-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="a61ee-111">Vérifiez que le client demande l’interface **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="a61ee-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="a61ee-112">Si une interface inappropriée est demandée, échouer et retourner MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="a61ee-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="a61ee-113">Créer un nouvel objet de recherche qui prend en charge l’interface **IMAPIContainer** .</span><span class="sxs-lookup"><span data-stu-id="a61ee-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="a61ee-114">À ce stade, un appel seront à la méthode **IMAPIProp::OpenProperty** de votre conteneur recherche pour extraire sa propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a61ee-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="a61ee-115">Votre fournisseur doit fournir un affichage tableau, généralement par le biais d’un appel à [BuildDisplayTable](builddisplaytable.md), qui décrit la boîte de dialogue Recherche avancée du conteneur.</span><span class="sxs-lookup"><span data-stu-id="a61ee-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="a61ee-116">MAPI affiche la boîte de dialogue de recherche permettant à l’utilisateur d’entrer les critères appropriés.</span><span class="sxs-lookup"><span data-stu-id="a61ee-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="a61ee-117">Lorsque l’utilisateur a terminé, MAPI appelle la méthode de [IMAPIProp::SetProps](imapiprop-setprops.md) du conteneur pour stocker les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="a61ee-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="a61ee-118">Un appel est effectué à la demande de table des matières du conteneur de votre recherche.</span><span class="sxs-lookup"><span data-stu-id="a61ee-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="a61ee-119">Renseignent la table des matières avec toutes les entrées dans le conteneur qui correspondent aux critères.</span><span class="sxs-lookup"><span data-stu-id="a61ee-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

