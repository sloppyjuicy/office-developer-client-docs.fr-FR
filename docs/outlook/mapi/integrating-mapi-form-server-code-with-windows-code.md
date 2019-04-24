---
title: Intégration de code de serveur de formulaire MAPI avec du code Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332178"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="baf99-103">Intégration de code de serveur de formulaire MAPI avec du code Windows</span><span class="sxs-lookup"><span data-stu-id="baf99-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="baf99-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="baf99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="baf99-105">Rappelez-vous que votre serveur de formulaire est une application Win32.</span><span class="sxs-lookup"><span data-stu-id="baf99-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="baf99-106">En tant que tel, certaines tâches relatives au chargement de votre serveur de formulaires dans la mémoire sont en cours de fermeture proprement.</span><span class="sxs-lookup"><span data-stu-id="baf99-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="baf99-107">Comme toutes les applications Windows, le point d'entrée de votre serveur de formulaires est la fonction **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="baf99-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="baf99-108">Cette fonction est l'endroit approprié pour effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="baf99-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="baf99-109">Création et inscription d'une classe de fenêtre afin que votre serveur de formulaire puisse interagir avec d'autres composants OLE.</span><span class="sxs-lookup"><span data-stu-id="baf99-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="baf99-110">Création et enregistrement d'une classe de fenêtre ou de classes pour les interfaces utilisateur de vos objets de formulaire.</span><span class="sxs-lookup"><span data-stu-id="baf99-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="baf99-111">Appel de la fonction [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="baf99-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="baf99-112">**MAPIInitialize** gère également l'initialisation OLE requise pour vous.</span><span class="sxs-lookup"><span data-stu-id="baf99-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="baf99-113">Cette opération doit être exécutée une fois par instance de votre serveur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="baf99-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="baf99-114">Inscription d'un atome global avec une représentation de chaîne de l'identificateur de classe (CLSID) du serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="baf99-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="baf99-115">Cet atome doit exister pendant la durée de vie du serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="baf99-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="baf99-116">Appel de la fonction OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) pour enregistrer la fabrique de classe de votre serveur de formulaires avec OLE.</span><span class="sxs-lookup"><span data-stu-id="baf99-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="baf99-117">Création d'une fenêtre principale pour recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="baf99-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="baf99-118">Cette fenêtre n'a probablement pas besoin d'être visible car l'utilisateur interagit avec les fenêtres spécifiques associées à des objets de formulaire individuels.</span><span class="sxs-lookup"><span data-stu-id="baf99-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="baf99-119">Toutefois, pendant le développement, la fenêtre principale peut être un emplacement pratique pour le débogage de la sortie ou du contrôle de votre serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="baf99-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="baf99-120">Création d'une boucle de message qui s'exécute pendant la durée de vie du serveur de formulaire, traduisant et distribuant les messages Windows en objets de formulaire actif.</span><span class="sxs-lookup"><span data-stu-id="baf99-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="baf99-121">Lorsque le serveur de formulaires se ferme, il doit effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="baf99-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="baf99-122">Appelez la fonction OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) pour révoquer l'enregistrement OLE de votre classe de message.</span><span class="sxs-lookup"><span data-stu-id="baf99-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="baf99-123">Appelez **MAPIUninitialize** pour fermer correctement la connexion du serveur de formulaire à MAPI.</span><span class="sxs-lookup"><span data-stu-id="baf99-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="baf99-124">Supprimez l'atome global qui contient la représentation sous forme de chaîne de l'identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="baf99-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="baf99-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baf99-125">See also</span></span>



[<span data-ttu-id="baf99-126">Écriture de code de serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="baf99-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

