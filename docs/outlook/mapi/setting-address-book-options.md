---
title: Définition des options du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417342"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="9bf92-103">Définition des options du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="9bf92-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="9bf92-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bf92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bf92-105">Vous pouvez définir trois propriétés qui décrivent les options d’utilisation du carnet d’adresses :</span><span class="sxs-lookup"><span data-stu-id="9bf92-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="9bf92-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9bf92-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="9bf92-107">La **PR_AB_SEARCH_PATH** est utilisée par [IAddrBook::ResolveName](iaddrbook-resolvename.md) pour déterminer les conteneurs à utiliser dans la résolution de noms et l’ordre dans le cas où ils doivent être impliqués.</span><span class="sxs-lookup"><span data-stu-id="9bf92-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="9bf92-108">Pour chaque conteneur dans **PR_AB_SEARCH_PATH,** **IAddrBook::ResolveName** appelle sa méthode [IABContainer::ResolveNames.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="9bf92-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="9bf92-109">Les conteneurs au début de **la PR_AB_SEARCH_PATH** sont recherchés avant les conteneurs à la fin de **la PR_AB_SEARCH_PATH**.</span><span class="sxs-lookup"><span data-stu-id="9bf92-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="9bf92-110">L’ordre de **recherche PR_AB_SEARCH_PATH** est spécifié à l’aide d’une structure [SRowSet,](srowset.md) la même structure que celle utilisée pour représenter les lignes d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="9bf92-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="9bf92-111">Vous pouvez afficher le chemin de recherche actuel en appelant la méthode [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) et le modifier en appelant la méthode [IAddrBook::SetSearchPath.](iaddrbook-setsearchpath.md)</span><span class="sxs-lookup"><span data-stu-id="9bf92-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="9bf92-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9bf92-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="9bf92-113">La **PR_AB_DEFAULT_DIR** est l’identificateur d’entrée du conteneur de carnet d’adresses à afficher initialement lorsque le carnet d’adresses est affiché.</span><span class="sxs-lookup"><span data-stu-id="9bf92-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="9bf92-114">Le paramètre de répertoire par défaut reste en vigueur jusqu’à ce que vous le modifiez en appelant la méthode [IAddrBook::SetDefaultDir.](iaddrbook-setdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="9bf92-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="9bf92-115">Vous pouvez afficher le répertoire par défaut en appelant la [méthode IAddrBook::GetDefaultDir.](iaddrbook-getdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="9bf92-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="9bf92-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9bf92-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="9bf92-117">Ces trois propriétés sont spéciales, car vous ne pouvez pas les utiliser à l’aide des méthodes **IMAPIProp** standard.</span><span class="sxs-lookup"><span data-stu-id="9bf92-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="9bf92-118">Au lieu de cela, vous devez utiliser **les méthodes IAddrBook.**</span><span class="sxs-lookup"><span data-stu-id="9bf92-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="9bf92-119">Étant donné qu’aucune de ces propriétés ne peut être modifiée avec **IMAPIProp::SetProps,** il n’est pas nécessaire d’appeler **IMAPIProp::SaveChanges** pour rendre les modifications permanentes.</span><span class="sxs-lookup"><span data-stu-id="9bf92-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="9bf92-120">Les modifications apportées via **les méthodes IAddrBook** prennent effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9bf92-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9bf92-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bf92-121">See also</span></span>



[<span data-ttu-id="9bf92-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9bf92-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

