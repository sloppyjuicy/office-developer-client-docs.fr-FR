---
title: Copie d'entrées de carnet d'adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333067"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="4787e-103">Copie d'entrées de carnet d'adresses</span><span class="sxs-lookup"><span data-stu-id="4787e-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="4787e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4787e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4787e-105">La méthode [IABContainer:: CopyEntries](iabcontainer-copyentries.md) de votre conteneur est appelée lorsqu'un ou plusieurs destinataires du même conteneur ou d'un autre conteneur doivent être copiés dans ce conteneur.</span><span class="sxs-lookup"><span data-stu-id="4787e-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="4787e-106">**CopyEntries** comporte quatre paramètres d'entrée: un tableau d'identificateurs d'entrée représentant les destinataires à copier, un handle de fenêtre pour l'indicateur de progression, un pointeur d'objet de progression et une valeur d'indicateurs.</span><span class="sxs-lookup"><span data-stu-id="4787e-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="4787e-107">Votre fournisseur doit afficher la progression si l'indicateur AB_NO_DIALOG n'est pas défini et utiliser l'objet Progress à partir du paramètre _lpProgress_ s'il n'est pas null.</span><span class="sxs-lookup"><span data-stu-id="4787e-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="4787e-108">Si _lpProgress_ est null, appelez [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) pour utiliser l'objet de progression MAPI.</span><span class="sxs-lookup"><span data-stu-id="4787e-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="4787e-109">Pour plus d'informations sur l'affichage de la progression, voir [affichage d'un indicateur de progression](mapi-progress-indicators.md).</span><span class="sxs-lookup"><span data-stu-id="4787e-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="4787e-110">En plus de AB_NO_DIALOG pour supprimer un indicateur de progression, un des deux autres indicateurs peut être défini pour demander un type de vérification d'entrées en double: CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="4787e-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="4787e-111">Les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT ne sont que des suggestions quant à la façon dont votre fournisseur détermine les entrées en double et peut être ignoré.</span><span class="sxs-lookup"><span data-stu-id="4787e-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="4787e-112">MAPI suggère que votre fournisseur implémente la prise en charge de ces indicateurs comme suit.</span><span class="sxs-lookup"><span data-stu-id="4787e-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="4787e-113">**Indicateur d'entrée en double**</span><span class="sxs-lookup"><span data-stu-id="4787e-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="4787e-114">**Implémentation suggérée**</span><span class="sxs-lookup"><span data-stu-id="4787e-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4787e-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="4787e-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="4787e-116">Vérifiez si le nom complet dans l'entrée à créer correspond au nom complet d'une entrée qui se trouve déjà dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="4787e-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="4787e-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="4787e-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="4787e-118">Vérifiez si le nom complet et la clé de recherche dans l'entrée à créer correspondent au nom complet et à la clé de recherche d'une entrée de conteneur.</span><span class="sxs-lookup"><span data-stu-id="4787e-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="4787e-119">Le dernier indicateur, CREATE_REPLACE, indique que la nouvelle entrée doit remplacer celle existante si votre fournisseur a déterminé qu'une entrée à créer est un doublon d'une entrée se trouvant déjà dans votre conteneur.</span><span class="sxs-lookup"><span data-stu-id="4787e-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="4787e-120">Si votre fournisseur est un carnet d'adresses personnel, incluez la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) dans chaque opération de copie.</span><span class="sxs-lookup"><span data-stu-id="4787e-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="4787e-121">L'inclusion de la table d'affichage des détails d'un destinataire copié permet à votre conteneur d'afficher les détails du destinataire au lieu d'appeler le conteneur d'origine pour créer l'affichage.</span><span class="sxs-lookup"><span data-stu-id="4787e-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="4787e-122">**Pour implémenter IABContainer:: CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="4787e-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="4787e-123">Déterminez si chaque identificateur d'entrée dans le paramètre _lpEntries_ est dans un format que votre fournisseur gère et, si ce n'est pas le cas, échoue et renvoie MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="4787e-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="4787e-124">Si un identificateur d'entrée représente un utilisateur de messagerie, une liste de distribution ou un conteneur géré par votre fournisseur:</span><span class="sxs-lookup"><span data-stu-id="4787e-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="4787e-125">Appelez la méthode [IMAPISupport:: OpenEntry](imapisupport-openentry.md) pour ouvrir le destinataire correspondant.</span><span class="sxs-lookup"><span data-stu-id="4787e-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="4787e-126">Copiez le destinataire dans votre conteneur.</span><span class="sxs-lookup"><span data-stu-id="4787e-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="4787e-127">Si l'identificateur d'entrée représente un destinataire étranger:</span><span class="sxs-lookup"><span data-stu-id="4787e-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="4787e-128">Appelez la méthode [IABContainer:: CreateEntry](iabcontainer-createentry.md) de votre conteneur pour créer un destinataire.</span><span class="sxs-lookup"><span data-stu-id="4787e-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="4787e-129">Définissez les propriétés initiales du nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="4787e-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="4787e-130">Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de l'objet pour l'enregistrer.</span><span class="sxs-lookup"><span data-stu-id="4787e-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="4787e-131">Mettez à jour la table des matières du conteneur pour refléter le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="4787e-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="4787e-132">Appeler [IMAPISupport:: Notify](imapisupport-notify.md) pour envoyer une notification de table aux clients inscrits.</span><span class="sxs-lookup"><span data-stu-id="4787e-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

