---
title: Implémentation d'une fonction de point d'entrée de fournisseur de services
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332990"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="14a81-103">Implémentation d'une fonction de point d'entrée de fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="14a81-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="14a81-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14a81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14a81-105">Chaque DLL de fournisseur de services possède une fonction de point d'entrée que MAPI appelle pour le charger.</span><span class="sxs-lookup"><span data-stu-id="14a81-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="14a81-106">N'oubliez pas que cette fonction de point d'entrée est différent de [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), la fonction de point d'entrée de la dll Win32.</span><span class="sxs-lookup"><span data-stu-id="14a81-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="14a81-107">Selon le type de votre fournisseur, la fonction de point d'entrée de fournisseur est conforme à un prototype différent.</span><span class="sxs-lookup"><span data-stu-id="14a81-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="14a81-108">MAPI définit différents prototypes de fonction de point d'entrée pour les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="14a81-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="14a81-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="14a81-109">**Provider**</span></span>|<span data-ttu-id="14a81-110">**Prototype de fonction de point d'entrée**</span><span class="sxs-lookup"><span data-stu-id="14a81-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14a81-111">Fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="14a81-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="14a81-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="14a81-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="14a81-113">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="14a81-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="14a81-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="14a81-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="14a81-115">Fournisseurs de carnets d'adresses</span><span class="sxs-lookup"><span data-stu-id="14a81-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="14a81-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="14a81-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="14a81-117">La plupart des fonctionnalités de ces prototypes sont les mêmes pour tous les types de fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="14a81-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="14a81-118">Les fournisseurs de carnet d'adresses, de banque de messages et de transport effectuent les deux tâches principales suivantes dans leurs fonctions de point d'entrée:</span><span class="sxs-lookup"><span data-stu-id="14a81-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="14a81-119">Vérifiez la version de l'interface du fournisseur de services (SPI) pour vous assurer que MAPI utilise une version compatible avec la version utilisée par votre fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="14a81-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="14a81-120">Utilisez le paramètre _lpulMAPIVer_ , qui contient la version de l'interface SPI MAPI et le paramètre _lpulProviderVer_ , qui contient votre version SPI, pour effectuer la vérification.</span><span class="sxs-lookup"><span data-stu-id="14a81-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="14a81-121">Ces paramètres sont des entiers non signés 32 bits composés de trois parties:</span><span class="sxs-lookup"><span data-stu-id="14a81-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="14a81-122">Les bits 24 à 31 représentent la version principale.</span><span class="sxs-lookup"><span data-stu-id="14a81-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="14a81-123">Les bits 16 à 23 représentent la version mineure.</span><span class="sxs-lookup"><span data-stu-id="14a81-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="14a81-124">Les bits 0 à 15 représentent l'identificateur de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="14a81-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="14a81-125">Bien que le numéro de version majeure change rarement, le numéro de version mineure change chaque fois que MAPI est publié et le SPI a changé.</span><span class="sxs-lookup"><span data-stu-id="14a81-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="14a81-126">L'identificateur de mise à jour est la version interne de Microsoft; elle permet de suivre les modifications pendant le processus de développement.</span><span class="sxs-lookup"><span data-stu-id="14a81-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="14a81-127">MAPI définit la constante CURRENT_SPI_VERSION, documentée dans le fichier d'en-tête Mapispi. h, pour indiquer la version de SPI actuelle.</span><span class="sxs-lookup"><span data-stu-id="14a81-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="14a81-128">Faites échouer votre vérification avec l'erreur MAPI_E_VERSION si vous utilisez une version du SPI qui est plus récente que la version utilisée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="14a81-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="14a81-129">Créer une instance d'un objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="14a81-129">Create an instance of a provider object.</span></span> <span data-ttu-id="14a81-130">Étant donné que votre fournisseur peut être démarré et initialisé plusieurs fois, vous devez créer une nouvelle instance chaque fois que cela se produit.</span><span class="sxs-lookup"><span data-stu-id="14a81-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="14a81-131">Les fournisseurs sont démarrés plusieurs fois lorsqu'ils apparaissent dans plusieurs profils qui sont utilisés simultanément par un ou plusieurs clients ou lorsqu'ils apparaissent plusieurs fois dans un même profil.</span><span class="sxs-lookup"><span data-stu-id="14a81-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="14a81-132">Tout comme le prototype de la fonction de point d'entrée diffère selon le type de votre fournisseur, c'est donc le type de l'objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="14a81-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="14a81-133">Si vous écrivez un fournisseur de carnets d'adresses, implémentez [IABProvider: IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="14a81-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="14a81-134">Si vous écrivez un fournisseur de banque de messages, implémentez [IMSProvider: IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="14a81-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="14a81-135">Pour plus d'informations, consultez la rubrique [chargement des fournisseurs de banques de messages](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="14a81-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="14a81-136">Si vous écrivez un fournisseur de transport, implémentez [IXPProvider: IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="14a81-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="14a81-137">Pour plus d'informations, consultez [la rubrique initialisation du fournisseur de transport](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="14a81-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14a81-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14a81-138">See also</span></span>



[<span data-ttu-id="14a81-139">Démarrage d'un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="14a81-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

