---
title: Ajout d’entrées de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421339"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="56c6f-103">Ajout d’entrées de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="56c6f-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="56c6f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56c6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56c6f-105">Pour ajouter un utilisateur de messagerie ou une liste de distribution à un conteneur, un client appelle [IAddrBook::NewEntry](iaddrbook-newentry.md) ou un fournisseur appelle [IMAPISupport::NewEntry](imapisupport-newentry.md) avec l’identificateur d’entrée du conteneur cible dans le paramètre _lpEIDContainer._</span><span class="sxs-lookup"><span data-stu-id="56c6f-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="56c6f-106">MAPI appelle à son tour la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) du conteneur pour créer l’entrée à l’aide d’un modèle unique à partir d’une table unique.</span><span class="sxs-lookup"><span data-stu-id="56c6f-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="56c6f-107">Un modèle unique permet au client de créer un destinataire d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="56c6f-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="56c6f-108">La plupart des champs sont modifiables.</span><span class="sxs-lookup"><span data-stu-id="56c6f-108">Most of the fields are editable.</span></span> <span data-ttu-id="56c6f-109">Le modèle pointé par le paramètre  _lpEntryID_ peut être celui que votre fournisseur fournit ou il peut s’agit d’un modèle provenant d’un fournisseur étranger, si votre fournisseur prend en charge les modèles étrangers.</span><span class="sxs-lookup"><span data-stu-id="56c6f-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="56c6f-110">Les implémentations **de CreateEntry** pour les fournisseurs qui peuvent créer des destinataires à partir d’un modèle étranger sont toujours plus complexes que les implémentations pour les fournisseurs qui ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="56c6f-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="56c6f-111">**Pour implémenter IABContainer::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="56c6f-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="56c6f-112">Déterminez le type d’identificateur d’entrée spécifié par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="56c6f-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="56c6f-113">Si l’identificateur d’entrée représente un modèle pour un utilisateur de messagerie, une liste de distribution ou un conteneur de carnet d’adresses qui appartient à votre fournisseur :</span><span class="sxs-lookup"><span data-stu-id="56c6f-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="56c6f-114">Créer et initialiser l’objet approprié.</span><span class="sxs-lookup"><span data-stu-id="56c6f-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="56c6f-115">Votre fournisseur peut définir certaines propriétés initiales si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="56c6f-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="56c6f-116">Ces propriétés dépendent du type de destinataire créé.</span><span class="sxs-lookup"><span data-stu-id="56c6f-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="56c6f-117">Renvoyer un pointeur vers l’implémentation de l’objet dans le contenu du _paramètre lppMAPIPropEntry._</span><span class="sxs-lookup"><span data-stu-id="56c6f-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="56c6f-118">Si l’identificateur d’entrée représente un modèle pour un fournisseur étranger :</span><span class="sxs-lookup"><span data-stu-id="56c6f-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="56c6f-119">Appelez [IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir l’objet étranger.</span><span class="sxs-lookup"><span data-stu-id="56c6f-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="56c6f-120">Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’objet, en passant NULL pour le tableau de balises de propriétés, pour récupérer ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="56c6f-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="56c6f-121">Modifiez le tableau de valeurs de propriétés renvoyé par **GetProps** en modifiant la balise de propriété en PR_NULL pour toutes les propriétés qui ne s’appliquent pas au nouvel objet et ne doivent pas être transférées.</span><span class="sxs-lookup"><span data-stu-id="56c6f-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="56c6f-122">Créez un identificateur d’entrée pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="56c6f-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="56c6f-123">Créez un objet du type approprié, utilisateur de messagerie ou liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="56c6f-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="56c6f-124">Initialise le nouvel objet en dérisant les propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="56c6f-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="56c6f-125">Vérifiez si l’objet étranger prend en **charge la PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="56c6f-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="56c6f-126">Si l’objet étranger prend en charge **PR_TEMPLATEID**, appelez [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour récupérer une interface d’objet de propriété auprès du fournisseur étranger et définissez le contenu du paramètre  _lppMAPIPropEntry_ sur l’implémentation de l’objet de propriété étrangère.</span><span class="sxs-lookup"><span data-stu-id="56c6f-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="56c6f-127">Si l’objet étranger ne prend **pas en charge PR_TEMPLATEID**, définissez le contenu du paramètre  _lppMAPIPropEntry_ sur l’implémentation du nouvel objet par votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="56c6f-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="56c6f-128">Appelez la [méthode IMAPIProp::SetProps](imapiprop-setprops.md) de l’objet pointé par le paramètre  _lppMAPIPropEntry_ pour définir les propriétés appropriées à partir de l’objet étranger.</span><span class="sxs-lookup"><span data-stu-id="56c6f-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

