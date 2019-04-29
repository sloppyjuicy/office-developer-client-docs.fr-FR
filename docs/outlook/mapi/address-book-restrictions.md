---
title: Restrictions du carnet d'adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432799"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="efc49-103">Restrictions du carnet d'adresses</span><span class="sxs-lookup"><span data-stu-id="efc49-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="efc49-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efc49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efc49-105">Les fournisseurs de carnets d'adresses sont requis pour prendre en charge trois types de restrictions sur les tables de contenu de leurs conteneurs:</span><span class="sxs-lookup"><span data-stu-id="efc49-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="efc49-106">Restrictions de propriété de nom ambigu</span><span class="sxs-lookup"><span data-stu-id="efc49-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="efc49-107">Restrictions de propriété de clé d'instance</span><span class="sxs-lookup"><span data-stu-id="efc49-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="efc49-108">Restrictions de contenu de nom d'affichage préfixé</span><span class="sxs-lookup"><span data-stu-id="efc49-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="efc49-109">Les restrictions de nom ambigus sont des restrictions de propriété utilisant la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) pour faire correspondre les noms des destinataires aux entrées dans les conteneurs du carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="efc49-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="efc49-110">La restriction de propriété **PR_ANR** est un type de recherche qui permet aux fournisseurs de carnet d'adresses de choisir la propriété correspondante la mieux adaptée à leur conteneur.</span><span class="sxs-lookup"><span data-stu-id="efc49-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="efc49-111">Par exemple, un fournisseur de carnet d'adresses peut implémenter la restriction **PR_ANR** en faisant correspondre les noms des destinataires à la propriété **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de chaque entrée de conteneur tandis qu'un autre fournisseur peut utiliser **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="efc49-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="efc49-112">MAPI recommande que les implémentations de la restriction **PR_ANR** soient équilibrées entre les performances et la satisfaction des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="efc49-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="efc49-113">La satisfaction des utilisateurs peut être compromise quand un fournisseur de carnet d'adresses implémente la restriction de telle sorte qu'il n'existe pas trop peu ou trop de correspondances.</span><span class="sxs-lookup"><span data-stu-id="efc49-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="efc49-114">Certains fournisseurs de carnets d'adresses prennent en charge ce qui est connu sous le nom de nom unique ou courant qui n'est pas affichable dans une boîte de dialogue, mais peut correspondre à une restriction de nom ambigu.</span><span class="sxs-lookup"><span data-stu-id="efc49-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="efc49-115">Une implémentation classique peut consister à analyser le nom d'affichage du destinataire en mots, ce qui correspond à n'importe quelle entrée contenant tous les mots.</span><span class="sxs-lookup"><span data-stu-id="efc49-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="efc49-116">Attention aux détails, tels que la sensibilité de la position de Word, la correspondance entre les mots non consécutifs et le choix des caractères de séparation.</span><span class="sxs-lookup"><span data-stu-id="efc49-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="efc49-117">Par exemple, si le nom à résoudre est «Bill L», une restriction **PR_ANR** classique sélectionnera les entrées suivantes, comme suit:</span><span class="sxs-lookup"><span data-stu-id="efc49-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="efc49-118">Billy Larson</span><span class="sxs-lookup"><span data-stu-id="efc49-118">Billy Larson</span></span>
    
- <span data-ttu-id="efc49-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="efc49-119">Bill Lee</span></span>
    
- <span data-ttu-id="efc49-120">Bill Logan Jr.</span><span class="sxs-lookup"><span data-stu-id="efc49-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="efc49-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="efc49-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="efc49-122">Les restrictions de clé d'instance, ou **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), sont utilisées dans l'implémentation des zones de liste utilisées dans les applications clientes pour l'affichage des tables MAPI.</span><span class="sxs-lookup"><span data-stu-id="efc49-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="efc49-123">Certaines implémentations de zone de liste permettent aux utilisateurs de sélectionner plusieurs sélections, de faire défiler vers le haut ou vers le bas et de revenir au premier élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="efc49-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="efc49-124">Pour implémenter ce comportement, les clients appellent [IMAPITable:: FindRow](imapitable-findrow.md), en transmettant une restriction de propriété sur la propriété **PR_INSTANCE_KEY** à la méthode.</span><span class="sxs-lookup"><span data-stu-id="efc49-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="efc49-125">Les fournisseurs de carnets d'adresses sont requis pour prendre en charge cette restriction.</span><span class="sxs-lookup"><span data-stu-id="efc49-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="efc49-126">Une autre fonctionnalité des zones de liste utilisées pour l'affichage des tableaux est la possibilité de positionner le curseur en fonction d'un ensemble de caractères de préfixe.</span><span class="sxs-lookup"><span data-stu-id="efc49-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="efc49-127">Lorsque l'utilisateur commence à taper des caractères de préfixe, le client place le curseur sur le premier élément qui commence par ces caractères.</span><span class="sxs-lookup"><span data-stu-id="efc49-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="efc49-128">Les clients implémentent cette fonctionnalité avec une restriction de contenu basée sur la propriété **PR_DISPLAY_NAME** et le niveau de fuzzing FL_PREFIX.</span><span class="sxs-lookup"><span data-stu-id="efc49-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efc49-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efc49-129">See also</span></span>



[<span data-ttu-id="efc49-130">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="efc49-130">MAPI Tables</span></span>](mapi-tables.md)

