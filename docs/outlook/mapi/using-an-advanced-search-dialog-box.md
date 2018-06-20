---
title: À l’aide d’une boîte de dialogue Recherche avancée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3c27b859f6d056d3b9a98bd4d71db8e500dff696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787447"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="22580-103">À l’aide d’une boîte de dialogue Recherche avancée</span><span class="sxs-lookup"><span data-stu-id="22580-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="22580-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22580-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22580-105">Certains conteneurs de carnet d’adresses prend en charge une fonction de recherche avancée qui permet aux clients d’effectuer une recherche sur les propriétés de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="22580-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="22580-106">Conteneurs du carnet d’adresses qui prennent en charge les recherches avancées ont une propriété de l’objet conteneur appelée **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="22580-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="22580-107">Cet objet conteneur fournit l’accès à un tableau d’affichage qui décrit la boîte de dialogue de recherche — une boîte de dialogue permet d’entrer et de modifier les critères de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="22580-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="22580-108">**Pour effectuer une recherche avancée sur un conteneur de carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="22580-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="22580-109">Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur spécifiant **PR_SEARCH** pour la balise de propriété et IID_IMAPIContainer pour l’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="22580-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="22580-110">Appeler la méthode **IMAPIProp::OpenProperty** de l’objet de la recherche, spécification **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) pour la balise de propriété et IID_IMAPITable pour l’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="22580-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="22580-111">Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’objet de la recherche pour définir des valeurs pour les propriétés à utiliser dans la recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="22580-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="22580-112">Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de l’objet de la recherche pour enregistrer les critères de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="22580-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="22580-113">Cette séquence d’appels entraîne une restriction étant disponible lorsqu’un client appelle la méthode **GetSearchCriteria** de l’objet de la recherche.</span><span class="sxs-lookup"><span data-stu-id="22580-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

