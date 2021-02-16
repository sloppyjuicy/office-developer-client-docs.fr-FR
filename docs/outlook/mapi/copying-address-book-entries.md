---
title: Copie des entrées du carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418742"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="79bbf-103">Copie des entrées du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="79bbf-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="79bbf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79bbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79bbf-105">La méthode [IABContainer::CopyEntries](iabcontainer-copyentries.md) de votre conteneur est appelée lorsqu’un ou plusieurs destinataires du même conteneur ou d’un autre conteneur doivent être copiés dans ce conteneur.</span><span class="sxs-lookup"><span data-stu-id="79bbf-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="79bbf-106">**CopyEntries** possède quatre paramètres d’entrée : un tableau d’identificateurs d’entrée représentant les destinataires à copier, une poignée de fenêtre pour l’indicateur de progression, un pointeur d’objet de progression et une valeur d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="79bbf-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="79bbf-107">Votre fournisseur doit afficher la progression si l’indicateur AB_NO_DIALOG n’est pas définie et utiliser l’objet de progression du paramètre  _lpProgress_ s’il n’est pas NULL.</span><span class="sxs-lookup"><span data-stu-id="79bbf-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="79bbf-108">Si  _lpProgress_ est NULL, appelez [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="79bbf-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="79bbf-109">Pour plus d’informations sur l’affichage de la progression, voir [Affichage d’un indicateur de progression.](mapi-progress-indicators.md)</span><span class="sxs-lookup"><span data-stu-id="79bbf-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="79bbf-110">En plus de AB_NO_DIALOG supprimer un indicateur de progression, l’un des deux autres indicateurs peut être définie pour demander un type de vérification des entrées en double : CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="79bbf-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="79bbf-111">Les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT sont uniquement des suggestions quant à la façon dont votre fournisseur détermine les entrées en double et peut être ignoré.</span><span class="sxs-lookup"><span data-stu-id="79bbf-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="79bbf-112">MAPI suggère à votre fournisseur d’implémenter la prise en charge de ces indicateurs comme suit.</span><span class="sxs-lookup"><span data-stu-id="79bbf-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="79bbf-113">**Indicateur d’entrée en double**</span><span class="sxs-lookup"><span data-stu-id="79bbf-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="79bbf-114">**Implémentation suggérée**</span><span class="sxs-lookup"><span data-stu-id="79bbf-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79bbf-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="79bbf-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="79bbf-116">Vérifiez si le nom complet de l’entrée à créer correspond au nom complet d’une entrée déjà dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="79bbf-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="79bbf-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="79bbf-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="79bbf-118">Vérifiez si le nom complet et la clé de recherche dans l’entrée à créer correspondent au nom d’affichage et à la clé de recherche d’une entrée de conteneur.</span><span class="sxs-lookup"><span data-stu-id="79bbf-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="79bbf-119">Le dernier indicateur, CREATE_REPLACE, indique que la nouvelle entrée doit remplacer l’entrée existante si votre fournisseur a déterminé qu’une entrée à créer est un doublon d’une entrée déjà dans votre conteneur.</span><span class="sxs-lookup"><span data-stu-id="79bbf-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="79bbf-120">Si votre fournisseur est un carnet d’adresses personnel, incluez la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) dans chaque opération de copie.</span><span class="sxs-lookup"><span data-stu-id="79bbf-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="79bbf-121">Inclure le tableau d’affichage des détails d’un destinataire copié permet à votre conteneur d’afficher les détails du destinataire au lieu d’appeler le conteneur d’origine pour créer l’affichage.</span><span class="sxs-lookup"><span data-stu-id="79bbf-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="79bbf-122">**Pour implémenter IABContainer::CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="79bbf-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="79bbf-123">Déterminez si chaque identificateur d’entrée dans le paramètre  _lpEntries_ est dans un format géré par votre fournisseur et, si ce n’est pas le cas, échouez et renvoyez MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="79bbf-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="79bbf-124">Si un identificateur d’entrée représente un utilisateur de messagerie, une liste de distribution ou un conteneur géré par votre fournisseur :</span><span class="sxs-lookup"><span data-stu-id="79bbf-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="79bbf-125">Appelez votre [méthode IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir le destinataire correspondant.</span><span class="sxs-lookup"><span data-stu-id="79bbf-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="79bbf-126">Copiez le destinataire dans votre conteneur.</span><span class="sxs-lookup"><span data-stu-id="79bbf-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="79bbf-127">Si l’identificateur d’entrée représente un destinataire étranger :</span><span class="sxs-lookup"><span data-stu-id="79bbf-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="79bbf-128">Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) de votre conteneur pour créer un destinataire.</span><span class="sxs-lookup"><span data-stu-id="79bbf-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="79bbf-129">Définissez les propriétés initiales sur le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="79bbf-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="79bbf-130">Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du nouvel objet pour l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="79bbf-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="79bbf-131">Mettez à jour la table des matières du conteneur pour refléter le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="79bbf-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="79bbf-132">Appelez [IMAPISupport::Notify](imapisupport-notify.md) pour envoyer une notification de table aux clients inscrits.</span><span class="sxs-lookup"><span data-stu-id="79bbf-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

