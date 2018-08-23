---
title: Intégration de code du serveur de formulaire MAPI avec du code Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b37ae47e40906342aeecf179848311556a7d4ba4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573991"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="3d4b3-103">Intégration de code du serveur de formulaire MAPI avec du code Windows</span><span class="sxs-lookup"><span data-stu-id="3d4b3-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="3d4b3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d4b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d4b3-105">Rappelez-vous que votre serveur de formulaire est une application Win32.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="3d4b3-106">Par conséquent, il existe certaines tâches liées à charger votre serveur de formulaire en mémoire et en quittant l’application proprement.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="3d4b3-107">Comme toutes les applications Windows, le point d’entrée pour le serveur de votre formulaire est la fonction **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="3d4b3-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="3d4b3-108">Cette fonction est l’emplacement approprié pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d4b3-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="3d4b3-109">Création et enregistrement d’une classe de fenêtre afin que votre serveur de formulaire peut interagir avec les autres composants OLE.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="3d4b3-110">Création et enregistrement d’une fenêtre ou les classes pour les interfaces utilisateur des objets de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="3d4b3-111">L’appel de la fonction [exécuter MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="3d4b3-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="3d4b3-112">**Exécuter MAPIInitialize** gère l’OLE initialisation requise, ainsi que.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="3d4b3-113">Il doit être effectuée une fois par instance de serveur de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="3d4b3-114">Inscription d’un atom globale avec une représentation de chaîne du serveur formulaire identificateurs de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="3d4b3-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="3d4b3-115">Cette atom doit exister pour la durée de vie du serveur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="3d4b3-116">L’appel de la fonction OLE [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) pour inscrire la fabrique de classe de votre serveur de formulaire avec OLE.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-116">Calling the OLE function [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="3d4b3-117">Création d’une fenêtre principale pour recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="3d4b3-118">Cette fenêtre n’a probablement pas besoin d’être visible, car l’utilisateur d’interagir avec les fenêtres spécifiques associées aux objets de formulaire individuel.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="3d4b3-119">Toutefois, lors du développement, la fenêtre principale peut être un emplacement pratique pour le débogage de sortie ou un contrôle de votre serveur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="3d4b3-120">Création d’une boucle de message qui s’exécute pendant la durée de vie du serveur de formulaire, traduction et répartir des messages windows aux objets du formulaire actif.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="3d4b3-121">La fermeture de votre serveur de formulaire, il doit effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d4b3-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="3d4b3-122">Appelez la fonction OLE [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) pour révoquer l’inscription de votre classe message OLE.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-122">Call the OLE function [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="3d4b3-123">Appelez **MAPIUninitialize** pour fermer correctement la connexion du serveur formulaire MAPI.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="3d4b3-124">Supprimer l’atom globale qui contient la représentation sous forme de chaîne de l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d4b3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d4b3-125">See also</span></span>



[<span data-ttu-id="3d4b3-126">Écriture de code du serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="3d4b3-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

