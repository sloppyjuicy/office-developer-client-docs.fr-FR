---
title: Implémentation d’une fonction de point d’entrée du fournisseur de carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409712"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a><span data-ttu-id="f4058-103">Implémentation d’une fonction de point d’entrée du fournisseur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="f4058-103">Implementing an Address Book Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="f4058-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4058-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4058-105">Lorsqu’une application cliente appelle [MAPILogonEx](mapilogonex.md) pour démarrer une session à l’aide d’un profil qui contient votre fournisseur de carnet d’adresses, MAPI charge votre fournisseur et tous les autres membres du profil.</span><span class="sxs-lookup"><span data-stu-id="f4058-105">When a client application calls [MAPILogonEx](mapilogonex.md) to begin a session using a profile that contains your address book provider, MAPI loads your provider and all others that are part of the profile.</span></span> <span data-ttu-id="f4058-106">MAPI apprend le nom de la fonction de point d’entrée de votre fournisseur en regardant dans le profil.</span><span class="sxs-lookup"><span data-stu-id="f4058-106">MAPI learns of the name of your provider's entry point function by looking in the profile.</span></span> <span data-ttu-id="f4058-107">N’oubliez pas que cette fonction n’est pas la même qu’une fonction de point d’entrée DLL ; voir la documentation relative **à DllMain** dans la documentation Win32.</span><span class="sxs-lookup"><span data-stu-id="f4058-107">Remember that this function is not the same as a DLL entry point function; see the documentation for **DllMain** in the Win32 documentation.</span></span> 
  
<span data-ttu-id="f4058-108">Il existe plusieurs entrées, dont certaines doivent apparaître dans le fichier de configuration mapisvc.inf, qui sont incluses dans la section profil de chaque fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f4058-108">There are several entries, some of which must appear in the mapisvc.inf configuration file, that are included in the profile section of every address book provider.</span></span> <span data-ttu-id="f4058-109">Le tableau suivant répertorie ces entrées de section de profil et indique si le fichier mapisvc.inf doit les inclure.</span><span class="sxs-lookup"><span data-stu-id="f4058-109">The following table lists these profile section entries and whether or not the mapisvc.inf file must include them.</span></span>
  
|<span data-ttu-id="f4058-110">**Entrée de section de profil**</span><span class="sxs-lookup"><span data-stu-id="f4058-110">**Profile section entry**</span></span>|<span data-ttu-id="f4058-111">**Condition requise pour mapisvc.inf**</span><span class="sxs-lookup"><span data-stu-id="f4058-111">**mapisvc.inf requirement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4058-112">PR_DISPLAY_NAME= _chaîne_</span><span class="sxs-lookup"><span data-stu-id="f4058-112">PR_DISPLAY_NAME= _string_</span></span> <br/> |<span data-ttu-id="f4058-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="f4058-113">Optional</span></span>  <br/> |
|<span data-ttu-id="f4058-114">PR_PROVIDER_DISPLAY= _chaîne_</span><span class="sxs-lookup"><span data-stu-id="f4058-114">PR_PROVIDER_DISPLAY= _string_</span></span> <br/> |<span data-ttu-id="f4058-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f4058-115">Required</span></span>  <br/> |
|<span data-ttu-id="f4058-116">PR_PROVIDER_DLL_NAME= _nom de fichier DLL_</span><span class="sxs-lookup"><span data-stu-id="f4058-116">PR_PROVIDER_DLL_NAME= _DLL filename_</span></span> <br/> |<span data-ttu-id="f4058-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f4058-117">Required</span></span>  <br/> |
|<span data-ttu-id="f4058-118">PR_RESOURCE_TYPE= _long_</span><span class="sxs-lookup"><span data-stu-id="f4058-118">PR_RESOURCE_TYPE= _long_</span></span> <br/> |<span data-ttu-id="f4058-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f4058-119">Required</span></span>  <br/> |
|<span data-ttu-id="f4058-120">PR_RESOURCE_FLAGS= masque _de bits_</span><span class="sxs-lookup"><span data-stu-id="f4058-120">PR_RESOURCE_FLAGS= _bitmask_</span></span> <br/> |<span data-ttu-id="f4058-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="f4058-121">Optional</span></span>  <br/> |
   
<span data-ttu-id="f4058-122">Votre fournisseur de carnet d’adresses peut placer ces informations dans un profil directement en appelant la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de sa section de profil ou indirectement en modifiant MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="f4058-122">Your address book provider can place this information into a profile directly by calling its profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method or indirectly by modifying MAPISVC.INF.</span></span> <span data-ttu-id="f4058-123">Les profils sont créés à l’aide des informations pertinentes dans MAPISVC. INF pour les fournisseurs de services ou services de messagerie sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="f4058-123">Profiles are built using the relevant information in MAPISVC.INF for the selected service providers or message services.</span></span> <span data-ttu-id="f4058-124">Pour plus d’informations sur l’organisation et le contenu de MAPISVC. INF, voir [Format de fichier de MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="f4058-124">For more information about the organization and contents of MAPISVC.INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
  
<span data-ttu-id="f4058-125">Le nom de la fonction de point d’entrée DLL de votre fournisseur de carnet d’adresses doit être [ABProviderInit](abproviderinit.md) et doit être conforme au prototype **ABProviderInit.**</span><span class="sxs-lookup"><span data-stu-id="f4058-125">The name of your address book provider's DLL entry point function must be [ABProviderInit](abproviderinit.md) and it must conform to the **ABProviderInit** prototype.</span></span> <span data-ttu-id="f4058-126">Effectuez les tâches suivantes dans la fonction de point d’entrée DLL de votre fournisseur :</span><span class="sxs-lookup"><span data-stu-id="f4058-126">Perform the following tasks in your provider's DLL entry point function:</span></span> 
  
- <span data-ttu-id="f4058-127">Vérifiez la version de l’interface du fournisseur de services (SPI) pour vous assurer que MAPI utilise une version compatible avec la version que votre fournisseur de carnet d’adresses utilise.</span><span class="sxs-lookup"><span data-stu-id="f4058-127">Check the version of the service provider interface (SPI) to make sure MAPI is using a version that is compatible with the version that your address book provider is using.</span></span>
    
- <span data-ttu-id="f4058-128">Ins instantiate an address book provider object.</span><span class="sxs-lookup"><span data-stu-id="f4058-128">Instantiate an address book provider object.</span></span>
    
<span data-ttu-id="f4058-129">N’appelez **pas MAPIInitialize** ou **MAPIUninitialize** dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f4058-129">Do not call either **MAPIInitialize** or **MAPIUninitialize** in this function.</span></span> 
  
<span data-ttu-id="f4058-130">La fonction de point d’entrée DLL ins instantie un objet fournisseur et retourne à MAPI un pointeur vers cet objet.</span><span class="sxs-lookup"><span data-stu-id="f4058-130">The DLL entry point function instantiates a provider object and returns to MAPI a pointer to that object.</span></span> 
  

