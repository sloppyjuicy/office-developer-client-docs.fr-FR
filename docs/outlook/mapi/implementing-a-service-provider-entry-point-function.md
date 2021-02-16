---
title: Implémentation d’une fonction de point d’entrée de fournisseur de services
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332990"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="7a39d-103">Implémentation d’une fonction de point d’entrée de fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="7a39d-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="7a39d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a39d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a39d-105">Chaque DLL de fournisseur de services possède une fonction de point d’entrée que MAPI appelle pour la charger.</span><span class="sxs-lookup"><span data-stu-id="7a39d-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="7a39d-106">Notez que cette fonction de point d’entrée n’est pas la même que [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), la fonction de point d’entrée DLL Win32.</span><span class="sxs-lookup"><span data-stu-id="7a39d-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="7a39d-107">Selon le type de votre fournisseur, votre fonction de point d’entrée de fournisseur est conforme à un prototype différent.</span><span class="sxs-lookup"><span data-stu-id="7a39d-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="7a39d-108">MAPI définit différents prototypes de fonction de point d’entrée pour les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="7a39d-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="7a39d-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="7a39d-109">**Provider**</span></span>|<span data-ttu-id="7a39d-110">**Prototype de fonction de point d’entrée**</span><span class="sxs-lookup"><span data-stu-id="7a39d-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a39d-111">Fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="7a39d-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="7a39d-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="7a39d-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="7a39d-113">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="7a39d-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="7a39d-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="7a39d-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="7a39d-115">Fournisseurs de carnets d’adresses</span><span class="sxs-lookup"><span data-stu-id="7a39d-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="7a39d-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="7a39d-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="7a39d-117">La plupart des fonctionnalités de ces prototypes sont identiques pour tous les types de fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="7a39d-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="7a39d-118">Les fournisseurs de carnet d’adresses, de magasin de messages et de transport effectuent les deux tâches principales suivantes dans leurs fonctions de point d’entrée :</span><span class="sxs-lookup"><span data-stu-id="7a39d-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="7a39d-119">Vérifiez la version de l’interface du fournisseur de services (SPI) pour vous assurer que MAPI utilise une version compatible avec la version que votre fournisseur de services utilise.</span><span class="sxs-lookup"><span data-stu-id="7a39d-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="7a39d-120">Utilisez le  _paramètre lpulMAPIVer,_ qui contient la version SPI MAPI, et le paramètre  _lpulProviderVer,_ qui contient votre version SPI, pour effectuer la vérification.</span><span class="sxs-lookup"><span data-stu-id="7a39d-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="7a39d-121">Ces paramètres sont des nombres entièrement non signés 32 bits composés de trois parties :</span><span class="sxs-lookup"><span data-stu-id="7a39d-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="7a39d-122">Les bits 24 à 31 représentent la version principale.</span><span class="sxs-lookup"><span data-stu-id="7a39d-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="7a39d-123">Les bits 16 à 23 représentent la version mineure.</span><span class="sxs-lookup"><span data-stu-id="7a39d-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="7a39d-124">Les bits 0 à 15 représentent l’identificateur de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7a39d-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="7a39d-125">Bien que le numéro de version principal change rarement, le numéro de version mineure change chaque fois que MAPI est publié et que spi a changé.</span><span class="sxs-lookup"><span data-stu-id="7a39d-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="7a39d-126">L’identificateur de mise à jour est la version de build interne de Microsoft . Il est utilisé pour suivre les modifications au cours du processus de développement.</span><span class="sxs-lookup"><span data-stu-id="7a39d-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="7a39d-127">MAPI définit la constante CURRENT_SPI_VERSION, documentée dans le fichier d’en-tête Mapispi.h, pour indiquer la version SPI actuelle.</span><span class="sxs-lookup"><span data-stu-id="7a39d-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="7a39d-128">Échec de votre vérification avec l’erreur MAPI_E_VERSION si vous utilisez une version de SPI plus récente que la version que MAPI utilise.</span><span class="sxs-lookup"><span data-stu-id="7a39d-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="7a39d-129">Créez une instance d’un objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7a39d-129">Create an instance of a provider object.</span></span> <span data-ttu-id="7a39d-130">Étant donné que votre fournisseur peut être démarré et initialisé plusieurs fois, vous devez créer une nouvelle instance chaque fois que cela se produit.</span><span class="sxs-lookup"><span data-stu-id="7a39d-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="7a39d-131">Les fournisseurs sont démarrés plusieurs fois lorsqu’ils apparaissent dans plusieurs profils utilisés simultanément par un ou plusieurs clients, ou lorsqu’ils apparaissent plusieurs fois dans un seul profil.</span><span class="sxs-lookup"><span data-stu-id="7a39d-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="7a39d-132">Tout comme le prototype de fonction de point d’entrée diffère en fonction du type de votre fournisseur, le type d’objet fournisseur le fait également.</span><span class="sxs-lookup"><span data-stu-id="7a39d-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="7a39d-133">Si vous écrivez un fournisseur de carnet d’adresses, implémentez [IABProvider : IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7a39d-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="7a39d-134">Si vous écrivez un fournisseur de magasins de messages, implémentez [IMSProvider : IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7a39d-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="7a39d-135">Pour plus d’informations, voir [Loading Message Store Providers](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="7a39d-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="7a39d-136">Si vous écrivez un fournisseur de transport, implémentez [IXPProvider : IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7a39d-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="7a39d-137">Pour plus d’informations, [voir Initialisation du fournisseur de transport.](initializing-the-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="7a39d-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a39d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a39d-138">See also</span></span>



[<span data-ttu-id="7a39d-139">Démarrage d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="7a39d-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

