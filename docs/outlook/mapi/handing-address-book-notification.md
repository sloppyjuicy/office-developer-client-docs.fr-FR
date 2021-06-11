---
title: Gestion des notifications du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413534"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="98de4-103">Gestion des notifications du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="98de4-103">Handing address book notification</span></span>
  
<span data-ttu-id="98de4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98de4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98de4-105">Les notifications de carnet d’adresses permettent à un client d’apprendre les événements qui se produisent à une entrée de carnet d’adresses ou à une entrée particulière.</span><span class="sxs-lookup"><span data-stu-id="98de4-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="98de4-106">Vous pouvez vous inscrire à ces notifications via le carnet d’adresses MAPI en appelant [IAddrBook::Advise](iaddrbook-advise.md) ou via la hiérarchie ou la table des matières d’un conteneur de carnet d’adresses en appelant [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="98de4-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="98de4-107">Spécifiez l’identificateur d’entrée d’un conteneur de carnet d’adresses, d’une liste de distribution ou d’un utilisateur de messagerie si vous vous inscrivez pour des notifications sur une entrée particulière et NULL si vous vous inscrivez pour les notifications sur l’intégralité du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="98de4-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="98de4-108">L’identificateur d’entrée doit représenter un utilisateur de messagerie ou une liste de distribution dans un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="98de4-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="98de4-109">**IAddrBook::Advise** examine cet identificateur d’entrée pour déterminer quel fournisseur de carnet d’adresses est responsable de l’objet correspondant et le fait suivre à la méthode [IABLogon::Advise](iablogon-advise.md) du fournisseur de carnet d’adresses approprié.</span><span class="sxs-lookup"><span data-stu-id="98de4-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="98de4-110">Les clients peuvent s’inscrire aux types d’événements suivants sur les entrées de carnet d’adresses :</span><span class="sxs-lookup"><span data-stu-id="98de4-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="98de4-111">Erreur critique</span><span class="sxs-lookup"><span data-stu-id="98de4-111">Critical error</span></span>
    
- <span data-ttu-id="98de4-112">L’un des événements d’objet (créé, modifié, supprimé, déplacé ou copié)</span><span class="sxs-lookup"><span data-stu-id="98de4-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="98de4-113">Tableau modifié</span><span class="sxs-lookup"><span data-stu-id="98de4-113">Table modified</span></span>
    
<span data-ttu-id="98de4-114">En règle générale, l’inscription se produit uniquement sur le contenu du conteneur de carnet d’adresses et les tables hiérarchiques.</span><span class="sxs-lookup"><span data-stu-id="98de4-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="98de4-115">Il est rare que les clients s’inscrivent avec l’utilisateur de messagerie de niveau inférieur et les objets de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="98de4-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="98de4-116">Cela est dû aux raisons :</span><span class="sxs-lookup"><span data-stu-id="98de4-116">This is because:</span></span>
  
- <span data-ttu-id="98de4-117">De nombreux fournisseurs de carnets d’adresses ne peuvent pas prendre en charge les notifications sur leurs utilisateurs de messagerie et leurs listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="98de4-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="98de4-118">Les notifications de tableau sont suffisantes pour suivre les modifications et les signaler aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="98de4-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

