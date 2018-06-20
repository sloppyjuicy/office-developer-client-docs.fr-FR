---
title: Implémentation d’une fonction de Point d’entrée de Service fournisseur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 632aff9c0f6fc60ee9730b5e43667b5b610ae8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784166"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="3e76e-103">Implémentation d’une fonction de Point d’entrée de Service fournisseur</span><span class="sxs-lookup"><span data-stu-id="3e76e-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="3e76e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e76e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e76e-105">Chaque fournisseur de services DLL a une entrée fonction appels MAPI pour le charger de point.</span><span class="sxs-lookup"><span data-stu-id="3e76e-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="3e76e-106">Sachez que cette fonction de point d’entrée n’est pas le même que [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), la fonction de point d’entrée DLL Win32.</span><span class="sxs-lookup"><span data-stu-id="3e76e-106">Be aware that this entry point function is not the same as [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="3e76e-107">Selon le type de votre fournisseur, la fonction de point d’entrée de votre fournisseur est conforme à un prototype différent.</span><span class="sxs-lookup"><span data-stu-id="3e76e-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="3e76e-108">MAPI définit les prototypes de fonction de point d’entrée différents pour les fournisseurs de service.</span><span class="sxs-lookup"><span data-stu-id="3e76e-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="3e76e-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="3e76e-109">**Provider**</span></span>|<span data-ttu-id="3e76e-110">**Prototype de fonction du point d’entrée**</span><span class="sxs-lookup"><span data-stu-id="3e76e-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e76e-111">Fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="3e76e-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="3e76e-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="3e76e-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="3e76e-113">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="3e76e-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="3e76e-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="3e76e-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="3e76e-115">Fournisseurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="3e76e-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="3e76e-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="3e76e-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="3e76e-117">La plupart des fonctionnalités de ces prototypes est la même pour tous les types de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="3e76e-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="3e76e-118">Carnet d’adresses, banque de messages et les fournisseurs de transport effectuer deux tâches principales suivantes dans leurs fonctions de point d’entrée :</span><span class="sxs-lookup"><span data-stu-id="3e76e-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="3e76e-119">Vérifier la version de l’interface de fournisseur de service (SPI) pour vous assurer que MAPI utilise une version compatible avec la version à l’aide de votre fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="3e76e-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="3e76e-120">Utilisez le paramètre _lpulMAPIVer_ , qui contient la version MAPI SPI et le paramètre _lpulProviderVer_ , qui contient votre version SPI, effectuer la vérification.</span><span class="sxs-lookup"><span data-stu-id="3e76e-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="3e76e-121">Ces paramètres sont des entiers non signés 32 bits composés de trois parties :</span><span class="sxs-lookup"><span data-stu-id="3e76e-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="3e76e-122">Bits 24 à 31 représentent la version principale.</span><span class="sxs-lookup"><span data-stu-id="3e76e-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="3e76e-123">Bits 16 à 23 représentent la version secondaire.</span><span class="sxs-lookup"><span data-stu-id="3e76e-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="3e76e-124">L’identificateur de la mise à jour représentent les bits 0 à 15.</span><span class="sxs-lookup"><span data-stu-id="3e76e-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="3e76e-125">Bien que le numéro de version majeur change rarement, la numéro de version mineur modifications chaque fois que MAPI est publié et le SPI a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="3e76e-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="3e76e-126">L’identificateur de la mise à jour est Microsoft interne build version ; Il est utilisé pour suivre les modifications apportées au cours du processus de développement.</span><span class="sxs-lookup"><span data-stu-id="3e76e-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="3e76e-127">MAPI définit la constante CURRENT_SPI_VERSION documentées dans le fichier d’en-tête Mapispi.h, pour indiquer la version actuelle de SPI.</span><span class="sxs-lookup"><span data-stu-id="3e76e-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="3e76e-128">Échoué à votre contrôle avec l’erreur MAPI_E_VERSION si vous utilisez une version de l’index SPI plus récente que la version à l’aide de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e76e-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="3e76e-129">Créez une instance d’un objet de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3e76e-129">Create an instance of a provider object.</span></span> <span data-ttu-id="3e76e-130">Étant donné que votre fournisseur peut être démarré et initialisé plusieurs fois, vous devez créer une nouvelle instance chaque fois que cela se produit.</span><span class="sxs-lookup"><span data-stu-id="3e76e-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="3e76e-131">Fournisseurs sont démarrés plusieurs fois lorsqu’ils s’affichent dans plusieurs profils qui sont utilisés simultanément par un ou plusieurs clients, ou lorsqu’ils s’affichent plusieurs fois dans un seul profil.</span><span class="sxs-lookup"><span data-stu-id="3e76e-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="3e76e-132">Comme le prototype de la fonction de point d’entrée diffère en fonction du type de votre fournisseur, donc ne le type d’objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3e76e-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="3e76e-133">Si vous écrivez un fournisseur de carnet d’adresses, implémentez [IABProvider : IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3e76e-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="3e76e-134">Si vous écrivez un fournisseur de banque de messages, implémentez [IMSProvider : IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3e76e-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="3e76e-135">Pour plus d’informations, voir [Chargement de fournisseurs de banque de Message](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="3e76e-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="3e76e-136">Si vous écrivez un fournisseur de transport, implémentez [IXPProvider : IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3e76e-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="3e76e-137">Pour plus d’informations, voir [l’initialisation du fournisseur de Transport](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3e76e-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e76e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e76e-138">See also</span></span>



[<span data-ttu-id="3e76e-139">Démarrage d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="3e76e-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

