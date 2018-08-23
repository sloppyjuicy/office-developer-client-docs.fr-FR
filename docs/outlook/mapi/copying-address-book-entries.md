---
title: Copie d’entrées de carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: eca0c9f63a4efaaa7f9fd066cf5dce451b8f6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565885"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="87473-103">Copie d’entrées de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="87473-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="87473-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87473-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87473-105">Méthode de [IABContainer::CopyEntries](iabcontainer-copyentries.md) de votre conteneur est appelée lorsque un ou plusieurs destinataires à partir du même ou un autre conteneur doivent être copiés dans ce conteneur.</span><span class="sxs-lookup"><span data-stu-id="87473-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="87473-106">**CopyEntries** comporte quatre paramètres d’entrée : un tableau d’identificateurs d’entrée représentant les destinataires à copier, un handle de fenêtre pour l’indicateur de progression, un pointeur d’objet de progression et une valeur pour les indicateurs.</span><span class="sxs-lookup"><span data-stu-id="87473-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="87473-107">Votre fournisseur doit afficher la progression si l’indicateur AB_NO_DIALOG n’est pas défini et que vous utilisez l’objet de l’avancement du paramètre _lpProgress_ si elle n’est pas NULL.</span><span class="sxs-lookup"><span data-stu-id="87473-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="87473-108">Si _lpProgress_ est NULL, appelez [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’objet de l’avancement MAPI.</span><span class="sxs-lookup"><span data-stu-id="87473-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="87473-109">Pour plus d’informations sur l’affichage de la progression, voir [affichant un indicateur de progression](mapi-progress-indicators.md).</span><span class="sxs-lookup"><span data-stu-id="87473-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="87473-110">Outre AB_NO_DIALOG pour supprimer un indicateur de progression, une des deux autres indicateurs peut être définie pour demander un type de vérification de l’entrée en double : CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="87473-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="87473-111">Les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT sont uniquement des suggestions quant au comment votre fournisseur détermine les entrées en double et peuvent être ignorés.</span><span class="sxs-lookup"><span data-stu-id="87473-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="87473-112">MAPI suggère que votre fournisseur de mettre en œuvre la prise en charge pour ces indicateurs comme suit.</span><span class="sxs-lookup"><span data-stu-id="87473-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="87473-113">**Indicateur d’entrée en double**</span><span class="sxs-lookup"><span data-stu-id="87473-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="87473-114">**Implémentation suggérée**</span><span class="sxs-lookup"><span data-stu-id="87473-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87473-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="87473-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="87473-116">Vérifiez si le nom complet de l’entrée à créer correspond au nom de l’affichage d’une entrée déjà dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="87473-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="87473-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="87473-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="87473-118">Vérifiez si le nom complet et la clé de recherche dans l’entrée doit être créé correspondent à la clé de recherche et le nom complet d’une entrée de conteneur.</span><span class="sxs-lookup"><span data-stu-id="87473-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="87473-119">Le dernier indicateur, CREATE_REPLACE, indique que la nouvelle entrée doit remplacer ce dernier si votre fournisseur a déterminé qu’une entrée à créer une copie d’une entrée déjà dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="87473-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="87473-120">Si votre fournisseur est un carnet d’adresses personnel, inclure la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) dans chaque opération de copie.</span><span class="sxs-lookup"><span data-stu-id="87473-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="87473-121">Y compris la table d’affichage Détails d’un destinataire copié permet de votre conteneur afficher les détails du destinataire au lieu d’avoir à appeler le conteneur d’origine pour créer l’affichage.</span><span class="sxs-lookup"><span data-stu-id="87473-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="87473-122">**Pour mettre en œuvre IABContainer::CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="87473-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="87473-123">Déterminer si chaque identificateur d’entrée dans le paramètre _lpEntries_ est dans un format qui gère votre fournisseur et si elle n’est pas, échouer et retourner MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="87473-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="87473-124">Si un identificateur d’entrée représente un utilisateur de messagerie, une liste de distribution ou un conteneur qui gère votre fournisseur :</span><span class="sxs-lookup"><span data-stu-id="87473-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="87473-125">Appeler votre méthode [IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir le destinataire correspondant.</span><span class="sxs-lookup"><span data-stu-id="87473-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="87473-126">Copiez le destinataire dans votre conteneur.</span><span class="sxs-lookup"><span data-stu-id="87473-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="87473-127">Si l’identificateur d’entrée représente un destinataire externe :</span><span class="sxs-lookup"><span data-stu-id="87473-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="87473-128">Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) de votre conteneur pour créer un nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="87473-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="87473-129">Définir les propriétés initiales sur le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="87473-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="87473-130">Appeler la nouvelle méthode l’objet [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="87473-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="87473-131">Mettre à jour la table de contenu du conteneur pour refléter le nouveau destinataire.</span><span class="sxs-lookup"><span data-stu-id="87473-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="87473-132">Appelez [IMAPISupport::Notify](imapisupport-notify.md) pour envoyer une notification de la table aux clients enregistrés.</span><span class="sxs-lookup"><span data-stu-id="87473-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

