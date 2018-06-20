---
title: Notification de carnet d’adresse de remise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f198be78dd36a6d0c9439da68ab322cd8cfa4172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783414"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="9ca56-103">Notification de carnet d’adresse de remise</span><span class="sxs-lookup"><span data-stu-id="9ca56-103">Handing address book notification</span></span>
  
<span data-ttu-id="9ca56-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ca56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ca56-105">Notifications de carnet d’adresse permettent à un client d’événements qui se produisent sur une entrée de carnet d’adresse ou à une entrée particulière.</span><span class="sxs-lookup"><span data-stu-id="9ca56-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="9ca56-106">Vous pouvez vous inscrire pour les notifications par le biais du carnet d’adresses MAPI en appelant [IAddrBook::Advise](iaddrbook-advise.md) ou hiérarchie d’un conteneur carnet d’adresses ou une table des matières en appelant [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="9ca56-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="9ca56-107">Spécifier l’identificateur d’entrée d’un conteneur de carnet d’adresses, une liste de distribution ou un utilisateur de messagerie si vous vous inscrivez pour les notifications sur une entrée particulière et la valeur NULL si l’inscription des notifications dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="9ca56-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="9ca56-108">L’identificateur d’entrée doit représenter un utilisateur de messagerie ou d’une liste de distribution dans un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="9ca56-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="9ca56-109">**IAddrBook::Advise** examine cet identificateur d’entrée pour déterminer quelle adresse fournisseur de carnet d’est responsable de l’objet correspondant et transfère l’appel à la méthode de [IABLogon::Advise](iablogon-advise.md) du fournisseur livre adresse appropriée.</span><span class="sxs-lookup"><span data-stu-id="9ca56-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="9ca56-110">Les clients peuvent s’inscrire pour les types suivants d’événements sur les entrées de carnet d’adresses :</span><span class="sxs-lookup"><span data-stu-id="9ca56-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="9ca56-111">Erreur critique</span><span class="sxs-lookup"><span data-stu-id="9ca56-111">Critical error</span></span>
    
- <span data-ttu-id="9ca56-112">Un des événements de l’objet (création, modifié, supprimé, déplacé ou copié)</span><span class="sxs-lookup"><span data-stu-id="9ca56-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="9ca56-113">Table modifiée</span><span class="sxs-lookup"><span data-stu-id="9ca56-113">Table modified</span></span>
    
<span data-ttu-id="9ca56-114">En règle générale, l’enregistrement se produit uniquement sur le contenu de conteneur du carnet d’adresses et les tables de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="9ca56-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="9ca56-115">Il est rare que les clients s’inscrire avec l’objets de liste de distribution et d’utilisateurs de messagerie de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="9ca56-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="9ca56-116">Il s’agit, car :</span><span class="sxs-lookup"><span data-stu-id="9ca56-116">This is because:</span></span>
  
- <span data-ttu-id="9ca56-117">Plusieurs fournisseurs de carnet d’adresses n’acceptent pas les notifications dans leurs listes de distribution et les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9ca56-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="9ca56-118">Notifications de table sont suffisantes pour le suivi des modifications et les signaler aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9ca56-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

