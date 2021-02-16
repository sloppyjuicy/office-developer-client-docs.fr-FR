---
title: Long-Term d’entrée de données
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409222"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="ab09e-103">Long-Term d’entrée de données</span><span class="sxs-lookup"><span data-stu-id="ab09e-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="ab09e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab09e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab09e-105">Un identificateur d’entrée à long terme est attribué par un fournisseur de services à un objet lorsqu’un objet nécessite un identificateur dont la durée de vie est prolongée.</span><span class="sxs-lookup"><span data-stu-id="ab09e-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="ab09e-106">Les identificateurs d’entrée à long terme sont toujours valides pendant des semaines ou des mois et peuvent être valides sur d’autres stations de travail, selon le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ab09e-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="ab09e-107">Les identificateurs à long terme créés par les fournisseurs de carnets d’adresses pour les destinataires personnalisés sont universellement valides.</span><span class="sxs-lookup"><span data-stu-id="ab09e-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="ab09e-108">Les identificateurs d’entrée à long terme sont affectés aux magasins de messages, aux dossiers, aux messages, aux conteneurs de carnet d’adresses, aux utilisateurs de messagerie et aux listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="ab09e-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="ab09e-109">Lorsque les applications clientes appellent la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de ces objets, il s’agit toujours d’un identificateur d’entrée à long terme qui est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="ab09e-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="ab09e-110">Les identificateurs d’entrée à long terme doivent être uniques dans toutes les magasins de messages du profil actif . par conséquent, lorsqu’un message ou un dossier est copié d’une magasin de messages vers une autre, un nouvel identificateur d’entrée doit lui être affecté.</span><span class="sxs-lookup"><span data-stu-id="ab09e-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="ab09e-111">Lorsqu’un objet de la boutique de messages est déplacé, le fournisseur de magasins de messages qui implémente le déplacement détermine si l’identificateur d’entrée d’origine reste valide.</span><span class="sxs-lookup"><span data-stu-id="ab09e-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="ab09e-112">Certains fournisseurs de services affectent de nouveaux identificateurs d’entrée aux objets déplacés ; d’autres non.</span><span class="sxs-lookup"><span data-stu-id="ab09e-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="ab09e-113">En cas de modification, le nouvel identificateur d’entrée est inclus dans les informations transmises aux clients lorsqu’ils sont avertis du déplacement.</span><span class="sxs-lookup"><span data-stu-id="ab09e-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="ab09e-114">En règle générale, les fournisseurs de magasins de messages implémentent le comportement suivant lorsqu’ils déplacent des dossiers :</span><span class="sxs-lookup"><span data-stu-id="ab09e-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="ab09e-115">Lorsqu’un dossier est déplacé d’une magasin de messages vers une autre de type différent, il est garanti que l’identificateur d’entrée change.</span><span class="sxs-lookup"><span data-stu-id="ab09e-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="ab09e-116">Lorsqu’un dossier est déplacé d’une magasin de messages vers une autre du même type, l’identificateur d’entrée change presque toujours.</span><span class="sxs-lookup"><span data-stu-id="ab09e-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="ab09e-117">Lorsqu’un dossier est déplacé vers un autre emplacement au sein de la même magasin de messages, l’identificateur d’entrée peut changer ou non, selon le fournisseur de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="ab09e-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="ab09e-118">En règle générale, le fait de renommer un dossier sans modifier son dossier parent n’entraîne pas la modification de l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ab09e-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab09e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab09e-119">See also</span></span>



[<span data-ttu-id="ab09e-120">Identificateurs d’entrée MAPI</span><span class="sxs-lookup"><span data-stu-id="ab09e-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

