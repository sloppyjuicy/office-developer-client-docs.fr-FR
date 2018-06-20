---
title: Définition des Options de livre adresse
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c64f84da6bece809176bf67985b6f55ce92414a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787135"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="51075-103">Définition des Options de livre adresse</span><span class="sxs-lookup"><span data-stu-id="51075-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="51075-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51075-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51075-105">Vous pouvez définir trois propriétés qui décrivent les options permettant d’utiliser le carnet d’adresses :</span><span class="sxs-lookup"><span data-stu-id="51075-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="51075-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51075-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="51075-107">La propriété **PR_AB_SEARCH_PATH** est utilisée par [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour déterminer les conteneurs à participer à la résolution de noms et l’ordre qu’ils doivent être impliqués.</span><span class="sxs-lookup"><span data-stu-id="51075-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="51075-108">Pour chaque conteneur dans **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** appelle la méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="51075-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="51075-109">Conteneurs au début de **PR_AB_SEARCH_PATH** sont recherchés avant les conteneurs à la fin de **PR_AB_SEARCH_PATH**.</span><span class="sxs-lookup"><span data-stu-id="51075-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="51075-110">L’ordre de recherche dans **PR_AB_SEARCH_PATH** est spécifié à l’aide d’une structure [SRowSet](srowset.md) , la même structure qui est utilisée pour représenter des lignes d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="51075-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="51075-111">Vous pouvez afficher le chemin de recherche actuel en appelant la méthode [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) et mettez-le en appelant la méthode [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) .</span><span class="sxs-lookup"><span data-stu-id="51075-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="51075-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51075-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="51075-113">La propriété **PR_AB_DEFAULT_DIR** est l’identificateur d’entrée du conteneur de carnet d’adresses à afficher à l’origine lorsque le carnet d’adresses est affichée.</span><span class="sxs-lookup"><span data-stu-id="51075-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="51075-114">Le paramètre de répertoire par défaut reste en vigueur jusqu'à ce que vous changiez en appelant la méthode [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) .</span><span class="sxs-lookup"><span data-stu-id="51075-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="51075-115">Vous pouvez afficher le répertoire par défaut en appelant la méthode [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) .</span><span class="sxs-lookup"><span data-stu-id="51075-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="51075-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="51075-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="51075-117">Ces trois propriétés sont spéciales, car vous ne pouvez pas travailler avec eux à l’aide des méthodes **IMAPIProp** standard.</span><span class="sxs-lookup"><span data-stu-id="51075-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="51075-118">Au lieu de cela, vous devez utiliser les méthodes **IAddrBook** .</span><span class="sxs-lookup"><span data-stu-id="51075-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="51075-119">Car aucune de ces propriétés peut être modifiée avec **IMAPIProp::SetProps**, il est inutile d’appeler **IMAPIProp::SaveChanges** pour apporter des modifications permanentes.</span><span class="sxs-lookup"><span data-stu-id="51075-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="51075-120">Modifications apportées à travers les méthodes **IAddrBook** prennent effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="51075-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51075-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51075-121">See also</span></span>



[<span data-ttu-id="51075-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51075-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

