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
ms.openlocfilehash: 99f47ee4fe990b0e77fcf868977b72d83bfdbac7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787251"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="515ac-103">Démarrage d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="515ac-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="515ac-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="515ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="515ac-105">À un moment donné après qu’un client démarre une session MAPI, votre fournisseur de services est démarré.</span><span class="sxs-lookup"><span data-stu-id="515ac-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="515ac-106">Fournisseurs de transport sont démarrés lorsqu’un client émet une demande de leurs services.</span><span class="sxs-lookup"><span data-stu-id="515ac-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="515ac-107">Fournisseurs de magasin de messages et du carnet d’adresses sont démarrés au cours du processus d’ouverture de session du client.</span><span class="sxs-lookup"><span data-stu-id="515ac-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="515ac-108">Un client appelle [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) pour charger chacun des fournisseurs de carnet d’adresses incluses dans le profil et [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) pour charger un fournisseur de magasin de message spécifique.</span><span class="sxs-lookup"><span data-stu-id="515ac-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="515ac-109">Fournisseurs de carnet d’adresses qui font partie d’un service de message sont démarrés avant les autres fournisseurs dans le service.</span><span class="sxs-lookup"><span data-stu-id="515ac-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="515ac-110">MAPI démarre chaque fournisseur de services dans le profil actif en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="515ac-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="515ac-111">Recherche le nom de la DLL dans le profil.</span><span class="sxs-lookup"><span data-stu-id="515ac-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="515ac-112">Vous devez enregistrer le nom de votre fournisseur de DLL dans le fichier de configuration Mapisvc.inf pour s’assurer qu’il apparaît dans le profil.</span><span class="sxs-lookup"><span data-stu-id="515ac-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="515ac-113">Lorsque votre fournisseur de services est ajouté à un profil, individuellement ou dans le cadre d’un service de message, toutes les sections **[Service Provider]** dans Mapisvc.inf qui s’appliquent à votre fournisseur sont copiés dans le profil.</span><span class="sxs-lookup"><span data-stu-id="515ac-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="515ac-114">Pour plus d’informations sur la structure du fichier Mapisvc.inf, voir le [Fichier de Format de fichier MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="515ac-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="515ac-115">L’appel de la fonction API Windows **LoadLibrary** pour charger la DLL.</span><span class="sxs-lookup"><span data-stu-id="515ac-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="515ac-116">Étant donné que les appels MAPI **LoadLibrary** soit chaque fois qu’elle utilise un fournisseur de services de DLL (indépendamment de si elle a déjà été chargé) ou uniquement la première fois, votre fournisseur de services ne doit pas apporter hypothèses quant au nombre de fois qu’elle sera chargée.</span><span class="sxs-lookup"><span data-stu-id="515ac-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="515ac-117">Pour chaque appel à **LoadLibrary**, MAPI effectue un appel à la fonction API Windows **FreeLibrary** lorsqu’un fournisseur de service que DLL n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="515ac-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="515ac-118">Appel de la fonction de point d’entrée pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="515ac-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="515ac-119">MAPI appelle la fonction de votre fournisseur de point d’entrée pour lancer le processus d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="515ac-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="515ac-120">Fonctions de point d’entrée Assurez-vous que vous utilisez une version de l’interface de fournisseur de service (SPI) qui est compatible avec la version en cours utilisée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="515ac-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="515ac-121">Ces fonctions renvoient également des pointeurs vers des objets de fournisseur nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="515ac-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="515ac-122">Pour plus d’informations sur la création d’une entrée de la fonction de point de votre fournisseur, voir [implémentation d’une fonction de Point de Service fournisseur de l’entrée](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="515ac-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="515ac-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="515ac-123">See also</span></span>



[<span data-ttu-id="515ac-124">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="515ac-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

