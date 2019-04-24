---
title: Utilisation d'une boîte de dialogue de recherche avancée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329665"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="9935f-103">Utilisation d'une boîte de dialogue de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="9935f-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="9935f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9935f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9935f-105">Certains conteneurs de carnet d'adresses prennent en charge une fonctionnalité de recherche avancée qui permet aux clients d'effectuer des recherches sur des propriétés autres que **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9935f-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="9935f-106">Les conteneurs de carnet d'adresses qui prennent en charge les recherches avancées disposent d'une propriété d'objet Container appelée **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9935f-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="9935f-107">Cet objet Container permet d'accéder à une table d'affichage qui décrit la boîte de dialogue de recherche (boîte de dialogue utilisée pour entrer et modifier les critères de recherche avancée).</span><span class="sxs-lookup"><span data-stu-id="9935f-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="9935f-108">**Pour effectuer une recherche avancée sur un conteneur de carnet d'adresses**</span><span class="sxs-lookup"><span data-stu-id="9935f-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="9935f-109">Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur en spécifiant **PR_SEARCH** pour la balise de propriété et IID_IMAPIContainer pour l'identificateur d'interface.</span><span class="sxs-lookup"><span data-stu-id="9935f-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="9935f-110">Appelez la méthode **IMAPIProp:: OpenProperty** de l'objet Search, en spécifiant **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) pour la balise de propriété et IID_IMAPITable pour l'identificateur d'interface.</span><span class="sxs-lookup"><span data-stu-id="9935f-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="9935f-111">Appelez la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) de l'objet de recherche pour établir des valeurs pour les propriétés à utiliser dans la recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="9935f-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="9935f-112">Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de l'objet de recherche pour enregistrer les critères de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="9935f-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="9935f-113">Cette séquence d'appels entraîne la disponibilité d'une restriction lorsqu'un client appelle la méthode **GetSearchCriteria** de l'objet de recherche.</span><span class="sxs-lookup"><span data-stu-id="9935f-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

