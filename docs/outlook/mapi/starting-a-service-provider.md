---
title: Démarrage d’un fournisseur de services
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439554"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="1df24-103">Démarrage d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="1df24-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="1df24-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1df24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1df24-105">À un moment donné, après qu’un client a démarré une session avec MAPI, votre fournisseur de services sera démarré.</span><span class="sxs-lookup"><span data-stu-id="1df24-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="1df24-106">Les fournisseurs de transport sont démarrés lorsqu’un client effectue une demande pour ses services.</span><span class="sxs-lookup"><span data-stu-id="1df24-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="1df24-107">Les fournisseurs de carnet d’adresses et de magasin de messages sont démarrés pendant le processus d’ouverture de ouverture de messagerie du client.</span><span class="sxs-lookup"><span data-stu-id="1df24-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="1df24-108">Un client appelle [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) pour charger chacun des fournisseurs de carnet d’adresses inclus dans le profil et [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) pour charger un fournisseur de magasin de messages spécifique.</span><span class="sxs-lookup"><span data-stu-id="1df24-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="1df24-109">Les fournisseurs de carnet d’adresses qui font partie d’un service de messagerie sont démarrés avant l’un des autres fournisseurs du service.</span><span class="sxs-lookup"><span data-stu-id="1df24-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="1df24-110">MAPI démarre chaque fournisseur de services dans le profil actif en suivant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1df24-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="1df24-111">Localisation du nom de sa DLL dans le profil.</span><span class="sxs-lookup"><span data-stu-id="1df24-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="1df24-112">Vous devez inscrire le nom de votre DLL de fournisseur dans le fichier de configuration Mapisvc.inf pour vous assurer qu’il apparaît dans le profil.</span><span class="sxs-lookup"><span data-stu-id="1df24-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="1df24-113">Lorsque votre fournisseur de services est ajouté à un profil, individuellement ou dans le cadre d’un service de messagerie, toutes les sections [Fournisseur de **services]** de Mapisvc.inf qui s’appliquent à votre fournisseur sont copiées dans le profil.</span><span class="sxs-lookup"><span data-stu-id="1df24-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="1df24-114">Pour plus d’informations sur la structure de Mapisvc.inf, voir Format de fichier [de MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="1df24-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="1df24-115">Appel de la Windows API **LoadLibrary pour** charger la DLL.</span><span class="sxs-lookup"><span data-stu-id="1df24-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="1df24-116">Étant donné que MAPI appelle **LoadLibrary** chaque fois qu’il utilise une DLL de fournisseur de services (qu’elle ait déjà été chargée ou seulement la première fois), votre fournisseur de services ne doit pas effectuer d’hypothèses sur le nombre de fois qu’il sera chargé.</span><span class="sxs-lookup"><span data-stu-id="1df24-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="1df24-117">Pour chaque appel à **LoadLibrary,** MAPI effectue un appel à la fonction d’API Windows **FreeLibrary** lorsqu’une DLL de fournisseur de services n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1df24-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="1df24-118">Appel de la fonction de point d’entrée pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1df24-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="1df24-119">MAPI appelle la fonction de point d’entrée de votre fournisseur pour lancer le processus d’inscription.</span><span class="sxs-lookup"><span data-stu-id="1df24-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="1df24-120">Les fonctions de point d’entrée garantissent que vous utilisez une version de l’interface du fournisseur de services (SPI) compatible avec la version utilisée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="1df24-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="1df24-121">Ces fonctions retournent également des pointeurs vers des objets fournisseur nouvellement créés.</span><span class="sxs-lookup"><span data-stu-id="1df24-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="1df24-122">Pour plus d’informations sur la création d’une fonction de point d’entrée pour votre fournisseur, voir [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="1df24-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1df24-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1df24-123">See also</span></span>



[<span data-ttu-id="1df24-124">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="1df24-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

