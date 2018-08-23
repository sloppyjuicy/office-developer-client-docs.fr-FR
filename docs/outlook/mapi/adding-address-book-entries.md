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
ms.openlocfilehash: d5b2aa2830e2721b9f895b22df12c9d712188625
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590133"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="86ebc-103">Ajout d’entrées de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="86ebc-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="86ebc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86ebc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86ebc-105">Pour ajouter un utilisateur de messagerie ou une liste de distribution à un conteneur ou d’un fournisseur, un client appelle [IAddrBook::NewEntry](iaddrbook-newentry.md) appelle [IMAPISupport::NewEntry](imapisupport-newentry.md) avec l’identificateur d’entrée du conteneur cible dans le paramètre _lpEIDContainer_ .</span><span class="sxs-lookup"><span data-stu-id="86ebc-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="86ebc-106">MAPI appelle ensuite la méthode de [IABContainer::CreateEntry](iabcontainer-createentry.md) du conteneur pour créer l’entrée à l’aide d’un modèle unique d’une table unique.</span><span class="sxs-lookup"><span data-stu-id="86ebc-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="86ebc-107">Un modèle unique autorise le client à créer un nouveau destinataire d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="86ebc-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="86ebc-108">La plupart des champs sont modifiable.</span><span class="sxs-lookup"><span data-stu-id="86ebc-108">Most of the fields are editable.</span></span> <span data-ttu-id="86ebc-109">Le modèle indiqué par le paramètre _lpEntryID_ peut être une que fournit votre fournisseur ou il peut être un modèle à partir d’un fournisseur externe, si votre fournisseur prend en charge les modèles étrangères.</span><span class="sxs-lookup"><span data-stu-id="86ebc-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="86ebc-110">Les implémentations de **CreateEntry** pour les fournisseurs qui peuvent créer des destinataires à partir d’un modèle étrangère sont toujours plus complexe que pour les fournisseurs qui ne peuvent pas les implémentations.</span><span class="sxs-lookup"><span data-stu-id="86ebc-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="86ebc-111">**Pour mettre en œuvre IABContainer::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="86ebc-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="86ebc-112">Déterminer le type d’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="86ebc-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="86ebc-113">Si l’identificateur d’entrée représente un modèle pour un utilisateur de messagerie, une liste de distribution ou un conteneur de carnet d’adresses appartenant à votre fournisseur de :</span><span class="sxs-lookup"><span data-stu-id="86ebc-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="86ebc-114">Créer et initialiser l’objet approprié.</span><span class="sxs-lookup"><span data-stu-id="86ebc-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="86ebc-115">Votre fournisseur peut définir certaines propriétés initiales si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="86ebc-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="86ebc-116">Ces propriétés dépendent du type de destinataire en cours de création.</span><span class="sxs-lookup"><span data-stu-id="86ebc-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="86ebc-117">Retourne un pointeur vers l’implémentation de l’objet dans le contenu du paramètre _lppMAPIPropEntry_ .</span><span class="sxs-lookup"><span data-stu-id="86ebc-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="86ebc-118">Si l’identificateur d’entrée représente un modèle pour un fournisseur externe :</span><span class="sxs-lookup"><span data-stu-id="86ebc-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="86ebc-119">Appelez [IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir l’objet étranger.</span><span class="sxs-lookup"><span data-stu-id="86ebc-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="86ebc-120">Appelez la méthode l’objet [IMAPIProp::GetProps](imapiprop-getprops.md) , en passant NULL pour le tableau de balise de propriété, pour récupérer ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="86ebc-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="86ebc-121">Modifier le tableau de valeurs de propriété renvoyé par **GetProps** en modifiant la balise de propriété pour PR_NULL pour toutes les propriétés qui ne s’applique pas au nouvel objet et ne doivent pas être transférées.</span><span class="sxs-lookup"><span data-stu-id="86ebc-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="86ebc-122">Créez un identificateur d’entrée pour le nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="86ebc-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="86ebc-123">Créer un nouvel objet de la saisie, soit messagerie utilisateur ou liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="86ebc-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="86ebc-124">Initialiser le nouvel objet en définissant les propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="86ebc-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="86ebc-125">Vérifier si l’objet étrangère prend en charge la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="86ebc-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="86ebc-126">Si l’objet étrangère prend en charge **PR_TEMPLATEID**, appelez [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour récupérer une interface d’objet de propriété à partir du fournisseur étranger et définir le contenu du paramètre _lppMAPIPropEntry_ à la propriété étrangère implémentation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="86ebc-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="86ebc-127">Si l’objet étranger ne gère pas **PR_TEMPLATEID**, définissez le contenu du paramètre _lppMAPIPropEntry_ pour l’implémentation de votre fournisseur du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="86ebc-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="86ebc-128">Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’objet désigné par le paramètre _lppMAPIPropEntry_ pour définir les propriétés appropriées de l’objet étranger.</span><span class="sxs-lookup"><span data-stu-id="86ebc-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

