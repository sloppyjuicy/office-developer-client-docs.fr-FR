---
title: L’implémentation d’une fonction Point d’entrée fournisseur adresse téléchargeable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b60a80bc0ede0c2800f6cfd98a98f498b93a1d8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784170"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="6aaf0-103">L’implémentation d’une fonction Point d’entrée fournisseur adresse téléchargeable</span><span class="sxs-lookup"><span data-stu-id="6aaf0-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="6aaf0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6aaf0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6aaf0-105">Lorsqu’un client application appelle [MAPILogonEx](mapilogonex.md) pour commencer une session à l’aide d’un profil qui contient votre fournisseur de carnet d’adresses, MAPI charge votre fournisseur et toutes les personnes qui font partie du profil.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="6aaf0-106">MAPI reçoit le nom de la fonction de point d’entrée de votre fournisseur en examinant le profil.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="6aaf0-107">N’oubliez pas que cette fonction est identique à une fonction de point d’entrée DLL ; consultez la documentation de **DllMain** dans la documentation de Win32.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="6aaf0-108">Il existe plusieurs entrées, certains d'entre eux doivent apparaître dans le fichier de configuration mapisvc.inf, qui sont incluses dans la section profil de chaque fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="6aaf0-109">Le tableau suivant répertorie les entrées de la section profil et si le fichier mapisvc.inf doit inclure.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="6aaf0-110">**Entrée de section de profil**</span><span class="sxs-lookup"><span data-stu-id="6aaf0-110">**Profile section entry**</span></span>|<span data-ttu-id="6aaf0-111">**exigence MAPISVC.inf**</span><span class="sxs-lookup"><span data-stu-id="6aaf0-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6aaf0-112">PR_DISPLAY_NAME = _chaîne_</span><span class="sxs-lookup"><span data-stu-id="6aaf0-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="6aaf0-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="6aaf0-113">Optional</span></span>  <br/> |
|<span data-ttu-id="6aaf0-114">PR_PROVIDER_DISPLAY = _chaîne_</span><span class="sxs-lookup"><span data-stu-id="6aaf0-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="6aaf0-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6aaf0-115">Required</span></span>  <br/> |
|<span data-ttu-id="6aaf0-116">PR_PROVIDER_DLL_NAME = _nom du fichier DLL_</span><span class="sxs-lookup"><span data-stu-id="6aaf0-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="6aaf0-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6aaf0-117">Required</span></span>  <br/> |
|<span data-ttu-id="6aaf0-118">PR_RESOURCE_TYPE = _long_</span><span class="sxs-lookup"><span data-stu-id="6aaf0-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="6aaf0-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6aaf0-119">Required</span></span>  <br/> |
|<span data-ttu-id="6aaf0-120">PR_RESOURCE_FLAGS = _masque de bits_</span><span class="sxs-lookup"><span data-stu-id="6aaf0-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="6aaf0-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="6aaf0-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="6aaf0-122">Votre fournisseur de carnet d’adresses permettre placer ces informations dans un profil directement en appelant la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la section de son profil ou indirectement en modifiant le fichier MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="6aaf0-123">Profils sont créées à l’aide des informations appropriées dans le fichier MAPISVC.inf. INF pour les fournisseurs de service sélectionnée ou les services de message.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="6aaf0-124">Pour plus d’informations sur l’organisation et le contenu du fichier MAPISVC.inf. INF, consultez le [Fichier de Format de fichier MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="6aaf0-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="6aaf0-125">Le nom de la fonction de point d’entrée DLL de votre fournisseur de carnet d’adresses doit être [ABProviderInit](abproviderinit.md) et il doit être conforme au prototype **ABProviderInit** .</span><span class="sxs-lookup"><span data-stu-id="6aaf0-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="6aaf0-126">Dans la fonction de point d’entrée DLL de votre fournisseur, effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="6aaf0-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="6aaf0-127">Vérifier la version de l’interface de fournisseur de service (SPI) pour vous assurer que MAPI utilise une version compatible avec la version à l’aide de votre fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="6aaf0-128">Instancier un objet de fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="6aaf0-129">N’appelez pas **l’exécuter MAPIInitialize** ou **MAPIUninitialize** dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="6aaf0-130">La fonction de point d’entrée DLL instancie un objet de fournisseur et renvoie à MAPI un pointeur vers cet objet.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

