---
title: Intégration d’applications de gestion Microsoft 365 Apps programme d’installation « Exécuter en un clic
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Découvrez comment intégrer le programme d Microsoft 365 Apps d’installation « En un clic » à une solution de gestion des logiciels.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297313"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a><span data-ttu-id="30b6d-103">Intégration d’applications de gestion Microsoft 365 Apps programme d’installation « Exécuter en un clic</span><span class="sxs-lookup"><span data-stu-id="30b6d-103">Integrating manageability applications with Microsoft 365 Apps Click-to-Run installer</span></span>

<span data-ttu-id="30b6d-104">Découvrez comment intégrer le programme d Microsoft 365 Apps d’installation « En un clic » à une solution de gestion des logiciels.</span><span class="sxs-lookup"><span data-stu-id="30b6d-104">Learn how to integrate the Microsoft 365 Apps Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="30b6d-105">Le Microsoft 365 Apps installer « En un clic » fournit une interface COM qui permet aux professionnels de l’informatique et aux solutions de gestion de logiciels de contrôler par programme la gestion des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="30b6d-105">The Microsoft 365 Apps Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="30b6d-106">Cette interface offre des fonctionnalités de gestion supplémentaires au-delà de ce qui est fourni par l’outil Office Deployment.</span><span class="sxs-lookup"><span data-stu-id="30b6d-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30b6d-107">Cet article s’applique Office applications qui utilisent le programme d’installation « En un clic ».</span><span class="sxs-lookup"><span data-stu-id="30b6d-107">This article applies to Office apps that use the Click-to-Run installer.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="30b6d-108">Intégration à l’outil « Click-to-Run</span><span class="sxs-lookup"><span data-stu-id="30b6d-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="30b6d-109">Pour utiliser cette interface, une application de gestion appelle l’interface COM et appelle les API exposées qui communiquent directement avec le service d’installation « En un clic ».</span><span class="sxs-lookup"><span data-stu-id="30b6d-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30b6d-110">Le programme d’installation Office « En un clic » peut être exécuté à partir de la ligne de commande avec des paramètres qui peuvent contrôler le comportement, comme documenté dans [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span><span class="sxs-lookup"><span data-stu-id="30b6d-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span></span> 
  
<span data-ttu-id="30b6d-111">**Voici un diagramme conceptuel de l’interface COM**</span><span class="sxs-lookup"><span data-stu-id="30b6d-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="30b6d-112">![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM Office programme d’installation « Exécuter en un clic")</span><span class="sxs-lookup"><span data-stu-id="30b6d-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="30b6d-113">Le Microsoft 365 Apps installer « En un clic » implémente une interface COM, **IUpdateNotify** inscrite dans CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="30b6d-113">The Microsoft 365 Apps Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="30b6d-114">Cette interface peut être invoquée comme suit :</span><span class="sxs-lookup"><span data-stu-id="30b6d-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="30b6d-115">L’appel réussit uniquement si l’appelant s’exécute avec des privilèges élevés, car le programme d’installation « En un clic » doit être exécuté avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="30b6d-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="30b6d-116">L’interface COM **IUpdateNotify** expose trois fonctions asynchrones responsables de la validation des commandes et des paramètres et de la planification de l’exécution avec le service d’installation « En un clic ».</span><span class="sxs-lookup"><span data-stu-id="30b6d-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="30b6d-117">Une autre méthode, **Status**, peut être utilisée pour obtenir des informations sur l’état de la dernière commande exécutée ou sur l’état de la commande en cours d’exécution (réussite, échec, codes d’erreur détaillés).</span><span class="sxs-lookup"><span data-stu-id="30b6d-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="30b6d-118">Il existe quatre états dans lesquels le service d’installation « En un clic » peut se trouver pendant son cycle de vie, au cours duquel les méthodes **IUpdateNotify** peuvent être appelées ; Redémarrage, inactivité, téléchargement et application.</span><span class="sxs-lookup"><span data-stu-id="30b6d-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="30b6d-119">**Voici le diagramme de la machine à états de l’interface COM**</span><span class="sxs-lookup"><span data-stu-id="30b6d-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="30b6d-120">![Diagramme d’état pour l’interface COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Diagramme d’état pour l’interface COM")</span><span class="sxs-lookup"><span data-stu-id="30b6d-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="30b6d-121">**Redémarrage**: lorsque l’ordinateur démarre, le service d’installation Démarrer en un clic n’est pas disponible pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="30b6d-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="30b6d-122">Un appel réussi à la méthode Status après un redémarrage eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="30b6d-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="30b6d-123">**Inactif :** Lorsque le programme d’installation En un clic est inactif, vous pouvez appeler :</span><span class="sxs-lookup"><span data-stu-id="30b6d-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="30b6d-124">**Appliquer**: installer le contenu précédemment téléchargé.</span><span class="sxs-lookup"><span data-stu-id="30b6d-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="30b6d-125">**Cancel**: renvoie  `0x800000e` « Une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="30b6d-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="30b6d-126">**Téléchargement**: télécharge le nouveau contenu sur le client pour une installation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="30b6d-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="30b6d-127">**État**: renvoie le résultat de la dernière action terminée ou un message d’erreur si l’action s’est terminée en échec.</span><span class="sxs-lookup"><span data-stu-id="30b6d-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="30b6d-128">S’il n’existe aucune action précédente, **l’état** renvoie  `eUPDATE_UNKNOWN` .</span><span class="sxs-lookup"><span data-stu-id="30b6d-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="30b6d-129">**Téléchargement :** Lorsque le programme d’installation En un clic est à l’état de téléchargement, vous pouvez appeler :</span><span class="sxs-lookup"><span data-stu-id="30b6d-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="30b6d-130">**Appliquer**: renvoie un **HRESULT** avec la valeur « Une méthode a été  `0x800000e` appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="30b6d-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="30b6d-131">**Cancel**: arrête le téléchargement et supprime le contenu partiellement téléchargé.</span><span class="sxs-lookup"><span data-stu-id="30b6d-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="30b6d-132">**Téléchargement**: renvoie un **HRESULT** avec la valeur « Une méthode a été  `0x800000e` appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="30b6d-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="30b6d-133">**Status**: renvoie **DOWNLOAD_WIP** pour indiquer que le travail de téléchargement est en cours.</span><span class="sxs-lookup"><span data-stu-id="30b6d-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="30b6d-134">**Application :** Lorsque le programme d’installation En un clic est en cours d’installation, téléchargez préalablement le contenu :</span><span class="sxs-lookup"><span data-stu-id="30b6d-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="30b6d-135">**Appliquer**: renvoie un **HRESULT** avec la valeur « Une méthode a été  `0x800000e` appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="30b6d-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="30b6d-136">**Cancel**: renvoie  `0x800000e` , l’action Appliquer ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="30b6d-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="30b6d-137">**Téléchargement**: renvoie un **HRESULT** avec la valeur « Une méthode a été  `0x800000e` appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="30b6d-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="30b6d-138">**État**: renvoie **APPLY_WIP** pour indiquer que le travail en cours d’application est en cours.</span><span class="sxs-lookup"><span data-stu-id="30b6d-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="30b6d-139">Étant donné qu’OfficeC2RCOM est un service COM+ et est chargé dynamiquement, vous devez appeler **CoCreateInstance** chaque fois que vous appelez une méthode sur cette classe pour vous assurer que vous obtenez le résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="30b6d-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="30b6d-140">Le service COM+ gère la création d’une instance si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="30b6d-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="30b6d-141">Lorsqu’une des méthodes est appelée pour la première fois, COM+ charge l’objet **IUpdateNotify** et l’exécute dans l’une dllhost.exe instances.</span><span class="sxs-lookup"><span data-stu-id="30b6d-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="30b6d-142">Le nouvel objet reste actif pendant environ 3 minutes en cas d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="30b6d-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="30b6d-143">Si un appel ultérieur est effectué dans les trois minutes suivant le dernier appel, l’objet **IUpdateNotify** reste chargé et une nouvelle instance n’est pas créée.</span><span class="sxs-lookup"><span data-stu-id="30b6d-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="30b6d-144">Si aucun appel n’est effectué dans les trois minutes, l’objet IUpdateNotify est déchargé et un nouvel objet **IUpdateNotify** est créé lors de l’appel suivant.</span><span class="sxs-lookup"><span data-stu-id="30b6d-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="30b6d-145">Guide de référence de l’API COM du programme d’installation « Exécuter en un clic »</span><span class="sxs-lookup"><span data-stu-id="30b6d-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="30b6d-146">Dans la documentation de référence de l’API suivante :</span><span class="sxs-lookup"><span data-stu-id="30b6d-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="30b6d-147">Les paramètres sont au format paire clé/valeur séparés par un espace.</span><span class="sxs-lookup"><span data-stu-id="30b6d-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="30b6d-148">Les paramètres ne sont pas sensibles à la cas.</span><span class="sxs-lookup"><span data-stu-id="30b6d-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="30b6d-149">Il existe une [liste de paramètres avec](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) la documentation disponible.</span><span class="sxs-lookup"><span data-stu-id="30b6d-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="30b6d-150">Le résumé de l’interface IUpdateNotify2 est désormais inclus.</span><span class="sxs-lookup"><span data-stu-id="30b6d-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="30b6d-151">Appliquer</span><span class="sxs-lookup"><span data-stu-id="30b6d-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="30b6d-152">Parameters</span><span class="sxs-lookup"><span data-stu-id="30b6d-152">Parameters</span></span>

-  <span data-ttu-id="30b6d-153">_displaylevel_: **true pour** afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false pour** masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="30b6d-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="30b6d-154">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="30b6d-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="30b6d-155">_forceappshutdown_: **true** pour forcer Office applications à s’arrêter immédiatement lorsque l’action  Appliquer est déclenchée ; **false** pour échouer si des applications Office sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="30b6d-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="30b6d-156">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="30b6d-156">The default is **false**.</span></span> <span data-ttu-id="30b6d-157">Pour [plus d’informations,](#bk_ApplyRemark) voir la remarque.</span><span class="sxs-lookup"><span data-stu-id="30b6d-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="30b6d-158">Si une Office’application est en  cours d’exécution lorsque l’action Appliquer est déclenchée, l’action  Appliquer échoue généralement.</span><span class="sxs-lookup"><span data-stu-id="30b6d-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="30b6d-159">Le passage à la méthode Apply entraîne l’arrêt immédiat des applications par le `forceappshutdown=true` service  **OfficeClickToRun** et l’application de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="30b6d-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="30b6d-160">L’utilisateur peut être en perte de données dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="30b6d-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="30b6d-161">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="30b6d-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30b6d-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="30b6d-162">**S_OK**</span></span> <br/> |<span data-ttu-id="30b6d-163">L’action a été envoyée au service « Click-To-Run » pour exécution.</span><span class="sxs-lookup"><span data-stu-id="30b6d-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="30b6d-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="30b6d-165">L’appelant n’est pas en cours d’exécution avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="30b6d-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="30b6d-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="30b6d-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="30b6d-167">Des paramètres non valides ont été passés.</span><span class="sxs-lookup"><span data-stu-id="30b6d-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="30b6d-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="30b6d-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="30b6d-169">L’action n’est pas autorisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="30b6d-169">Action is not allowed at this time.</span></span> <span data-ttu-id="30b6d-170">Pour [plus d’informations,](#bk_ApplyRemark) voir la remarque.</span><span class="sxs-lookup"><span data-stu-id="30b6d-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="30b6d-171">Remarques</span><span class="sxs-lookup"><span data-stu-id="30b6d-171">Remarks</span></span>

- <span data-ttu-id="30b6d-172">Si une Office’application est  en cours d’exécution lorsque l’action Appliquer est déclenchée, **l’action** Appliquer échoue.</span><span class="sxs-lookup"><span data-stu-id="30b6d-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="30b6d-173">La transmission à la méthode Apply entraîne l’arrêt immédiat par le `forceappshutdown=true` service  **OfficeClickToRun** de toutes les applications Office en cours d’exécution et applique la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="30b6d-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="30b6d-174">L’utilisateur peut faire l’expérience des données car il n’est pas invité à enregistrer les modifications apportées aux documents ouverts.</span><span class="sxs-lookup"><span data-stu-id="30b6d-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="30b6d-175">Cette action ne peut être déclenchée que lorsque l’état COM est l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="30b6d-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="30b6d-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="30b6d-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="30b6d-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="30b6d-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="30b6d-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="30b6d-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="30b6d-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="30b6d-182">Si vous appelez la méthode **Apply** sans télécharger  préalablement le contenu, la méthode **Apply** indique Réussite car elle n’a détecté aucun résultat à appliquer et a terminé le **processus Appliquer** avec succès.</span><span class="sxs-lookup"><span data-stu-id="30b6d-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="30b6d-183">Annuler</span><span class="sxs-lookup"><span data-stu-id="30b6d-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="30b6d-184">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="30b6d-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30b6d-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="30b6d-185">S_OK</span></span>  <br/> |<span data-ttu-id="30b6d-186">L’action a été envoyée au service « Click-to-Run » pour exécution.</span><span class="sxs-lookup"><span data-stu-id="30b6d-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="30b6d-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="30b6d-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="30b6d-188">L’action n’est pas autorisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="30b6d-188">Action is not allowed at this time.</span></span> <span data-ttu-id="30b6d-189">Pour plus [d’informations,](#bk_CancelRemarks) voir la section Remarques</span><span class="sxs-lookup"><span data-stu-id="30b6d-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="30b6d-190">Remarques</span><span class="sxs-lookup"><span data-stu-id="30b6d-190">Remarks</span></span>

- <span data-ttu-id="30b6d-191">Cette méthode ne peut être déclenchée que lorsque l’ID d’état COM **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="30b6d-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="30b6d-192">Il tentera d’annuler l’action de téléchargement actuelle.</span><span class="sxs-lookup"><span data-stu-id="30b6d-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="30b6d-193">L’état COM change en **eDOWNLOAD_CANCELLING** et finit par **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="30b6d-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="30b6d-194">L’état COM retourne **E_ILLEGAL_METHOD_CALL** si déclenché à tout autre moment.</span><span class="sxs-lookup"><span data-stu-id="30b6d-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="30b6d-195">Télécharger</span><span class="sxs-lookup"><span data-stu-id="30b6d-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="30b6d-196">Parameters</span><span class="sxs-lookup"><span data-stu-id="30b6d-196">Parameters</span></span>

-  <span data-ttu-id="30b6d-197">_displaylevel_: **true pour** afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false pour** masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="30b6d-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="30b6d-198">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="30b6d-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="30b6d-199">_updatebaseurl_: URL de l’autre source de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="30b6d-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="30b6d-200">_updatetoversion_: version vers Office mise à jour.</span><span class="sxs-lookup"><span data-stu-id="30b6d-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="30b6d-201">Définissez ce paramètre si vous souhaitez mettre à jour une version antérieure à la version actuellement installée.</span><span class="sxs-lookup"><span data-stu-id="30b6d-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="30b6d-202">_downloadsource_: CLSID de l’implémentation **IBackgroundCopyManager** personnalisée (gestionnaire BITS).</span><span class="sxs-lookup"><span data-stu-id="30b6d-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="30b6d-203">_contentid_: identifie le contenu à télécharger à partir du serveur de contenu via le gestionnaire BITS personnalisé.</span><span class="sxs-lookup"><span data-stu-id="30b6d-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="30b6d-204">Cette valeur est transmise par le biais de l’interface BITS pour interprétation.</span><span class="sxs-lookup"><span data-stu-id="30b6d-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="30b6d-205">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="30b6d-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30b6d-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="30b6d-206">**S_OK**</span></span> <br/> |<span data-ttu-id="30b6d-207">L’action a été envoyée au service « Click-To-Run » pour exécution.</span><span class="sxs-lookup"><span data-stu-id="30b6d-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="30b6d-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="30b6d-209">L’appelant n’est pas en cours d’exécution avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="30b6d-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="30b6d-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="30b6d-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="30b6d-211">Des paramètres non valides ont été passés.</span><span class="sxs-lookup"><span data-stu-id="30b6d-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="30b6d-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="30b6d-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="30b6d-213">L’action n’est pas autorisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="30b6d-213">Action is not allowed at this time.</span></span> <span data-ttu-id="30b6d-214">Pour [plus d’informations,](#bk_DownloadRemark) voir la remarque.</span><span class="sxs-lookup"><span data-stu-id="30b6d-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="30b6d-215">Remarques</span><span class="sxs-lookup"><span data-stu-id="30b6d-215">Remarks</span></span>

- <span data-ttu-id="30b6d-216">Vous devez spécifier  _downloadsource_ et  _contentid_ en tant que paire.</span><span class="sxs-lookup"><span data-stu-id="30b6d-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="30b6d-217">Si ce n’est **pas le cas, la** méthode Download E_INVALIDARG erreur. </span><span class="sxs-lookup"><span data-stu-id="30b6d-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="30b6d-218">Si  _downloadsource,_  _contentid_ et  _updatebaseurl_ sont fournis,  _updatebaseurl_ sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="30b6d-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="30b6d-219">Cette action ne peut être déclenchée que lorsque l’état COM est l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="30b6d-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="30b6d-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="30b6d-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="30b6d-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="30b6d-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="30b6d-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="30b6d-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="30b6d-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="30b6d-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="30b6d-226">Si vous appelez la méthode **Apply** sans contenu  téléchargé précédemment, la méthode **Apply** indique Réussite car elle n’a détecté aucun résultat à appliquer et a terminé le processus **Appliquer** avec succès.</span><span class="sxs-lookup"><span data-stu-id="30b6d-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="30b6d-227">Exemples</span><span class="sxs-lookup"><span data-stu-id="30b6d-227">Examples</span></span>

- <span data-ttu-id="30b6d-228">Pour télécharger le contenu à partir du gestionnaire BITS personnalisé : appelez la fonction **download()** en passant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="30b6d-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="30b6d-229">Pour télécharger le contenu à partir de la Office réseau de distribution de contenu (CDN) : appelez la fonction **download()** sans spécifier les paramètres _downloadsource,_ _contentid_ ou _updatebaseurl._</span><span class="sxs-lookup"><span data-stu-id="30b6d-229">To download the content from the Office Content Delivery Network (CDN): Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="30b6d-230">Pour télécharger le contenu à partir d’un emplacement personnalisé : appelez la fonction **download()** en passant le paramètre suivant :</span><span class="sxs-lookup"><span data-stu-id="30b6d-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="30b6d-231">Statut</span><span class="sxs-lookup"><span data-stu-id="30b6d-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="30b6d-232">Parameters</span><span class="sxs-lookup"><span data-stu-id="30b6d-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="30b6d-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="30b6d-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="30b6d-234">Pointeur vers une UPDATE_STATUS_REPORT structure.</span><span class="sxs-lookup"><span data-stu-id="30b6d-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="30b6d-235">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="30b6d-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30b6d-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="30b6d-236">**S_OK**</span></span> <br/> |<span data-ttu-id="30b6d-237">La **méthode Status** renvoie toujours ce résultat.</span><span class="sxs-lookup"><span data-stu-id="30b6d-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="30b6d-238">Examinez  `UPDATE_STATUS_RESULT` la structure pour l’état de l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="30b6d-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="30b6d-239">Remarques</span><span class="sxs-lookup"><span data-stu-id="30b6d-239">Remarks</span></span>

- <span data-ttu-id="30b6d-240">Le champ d’état du  `UPDATE_STATUS_REPORT` champ contient l’état de l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="30b6d-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="30b6d-241">L’une des valeurs d’état suivantes est renvoyée :</span><span class="sxs-lookup"><span data-stu-id="30b6d-241">One of the following status values is returned:</span></span> 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- <span data-ttu-id="30b6d-242">Si la dernière commande a entraîné une erreur, le champ d’erreur contient des informations détaillées  `UPDATE_STATUS_REPORT` sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="30b6d-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="30b6d-243">Deux types de codes d’erreur sont renvoyés à partir de la **méthode Status.**</span><span class="sxs-lookup"><span data-stu-id="30b6d-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="30b6d-244">Si l’erreur est inférieure à , l’erreur est l’un des  `UPDATE_ERROR_CODE::eUNKNOWN` codes d’erreur prédéfin définis suivants :</span><span class="sxs-lookup"><span data-stu-id="30b6d-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  <span data-ttu-id="30b6d-245">Si le code d’erreur de retour est supérieur au  `UPDATE_ERROR_CODE::eUNKNOWN` **HRESULT** d’un appel de fonction qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="30b6d-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="30b6d-246">Pour extraire la soustraction HRESULT  `UPDATE_ERROR_CODE::eUNKNOWN` de la valeur renvoyée dans le champ d’erreur du  `UPDATE_STATUS_REPORT` .</span><span class="sxs-lookup"><span data-stu-id="30b6d-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="30b6d-247">La liste complète des valeurs d’état et d’erreur peut être vue en inspectant la bibliothèque de types **IUpdateNotify** incorporée dans OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="30b6d-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="30b6d-248">Le champ contentid est utilisé  pour les appels à **l’état** une fois le téléchargement lancé et renvoie le contentid qui a été transmis à l’appel **de** téléchargement.</span><span class="sxs-lookup"><span data-stu-id="30b6d-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="30b6d-249">Il est préférable d’initialiser ce champ sur **null** avant d’appeler  la méthode **Status,** puis de vérifier la valeur une fois l’état renvoyé.</span><span class="sxs-lookup"><span data-stu-id="30b6d-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="30b6d-250">Si la valeur est toujours **null,** cela signifie qu’il n’y a aucun contentid à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="30b6d-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="30b6d-251">Si la valeur n’est pas **null,** vous devez la libérer avec un appel à **SysFreeString()**.</span><span class="sxs-lookup"><span data-stu-id="30b6d-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="30b6d-252">Voici un extrait de code de la façon d’appeler **l’état** après le **téléchargement.**</span><span class="sxs-lookup"><span data-stu-id="30b6d-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="30b6d-253">Résumé de l’interface IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="30b6d-253">Summary of IUpdateNotify2 interface</span></span>

<span data-ttu-id="30b6d-254">À partir de la version [16.0.8208.6352], nous avons ajouté une nouvelle interface **IUpdateNotify2.**</span><span class="sxs-lookup"><span data-stu-id="30b6d-254">From version [16.0.8208.6352] we have added a new **IUpdateNotify2** interface.</span></span> 
  
- <span data-ttu-id="30b6d-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="30b6d-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="30b6d-256">Cette interface a également hébergé l’interface IUpdateNotify d’origine pour assurer la compatibilité ascendante.</span><span class="sxs-lookup"><span data-stu-id="30b6d-256">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="30b6d-257">Par conséquent, si vous utilisez cette interface, vous avez accès à toutes les méthodes fournies dans l’interface **UpdateNotifyObject.**</span><span class="sxs-lookup"><span data-stu-id="30b6d-257">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="30b6d-258">Nouvelles méthodes ajoutées à IUpdateNotify2 :</span><span class="sxs-lookup"><span data-stu-id="30b6d-258">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="30b6d-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="30b6d-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="30b6d-260">Obtenir la liste des applications de blocage des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="30b6d-260">Get updates blocking apps list.</span></span> <span data-ttu-id="30b6d-261">Cet appel retourne l’exécution Office applications qui bloquent le processus de mise à jour de poursuivre.</span><span class="sxs-lookup"><span data-stu-id="30b6d-261">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="30b6d-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="30b6d-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="30b6d-263">Obtenir Office de déploiement.</span><span class="sxs-lookup"><span data-stu-id="30b6d-263">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="30b6d-264">Si vous souhaitez utiliser les nouvelles méthodes, vous devez vous assurer que :</span><span class="sxs-lookup"><span data-stu-id="30b6d-264">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="30b6d-265">Votre version C2R est plus récente que la build ci-dessus ( \> = build de bifurcation de juin).</span><span class="sxs-lookup"><span data-stu-id="30b6d-265">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="30b6d-266">Utilisez UpdateNotifyObject2, au lieu de **UpdateNotifyObject** pour appeler **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="30b6d-266">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="30b6d-267">Si vous n’utilisez aucune des nouvelles méthodes, vous n’avez rien à modifier.</span><span class="sxs-lookup"><span data-stu-id="30b6d-267">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="30b6d-268">Toutes les méthodes existantes fonctionneront de la même manière qu’auparavant.</span><span class="sxs-lookup"><span data-stu-id="30b6d-268">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="30b6d-269">Mise en œuvre de l’interface BITS</span><span class="sxs-lookup"><span data-stu-id="30b6d-269">Implementing the BITS interface</span></span>

<span data-ttu-id="30b6d-270">Le [service BITS (Background Intelligent Transfer Service)](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) est un service fourni par Microsoft pour transférer des fichiers entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="30b6d-270">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="30b6d-271">BITS est l’un des canaux Office le programme d’installation « Exécuter en un clic » peut utiliser pour télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="30b6d-271">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="30b6d-272">Par défaut, le programme d Microsoft 365 Apps d’installation « En un clic » utilise l’implémentation intégrée de BITS du Windows pour télécharger le contenu à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="30b6d-272">By default, the Microsoft 365 Apps Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="30b6d-273">En fournissant une implémentation BITS personnalisée à la méthode **download()** de l’interface **IUpdateNotify,** votre logiciel de gestion peut contrôler où et comment le client télécharge le contenu.</span><span class="sxs-lookup"><span data-stu-id="30b6d-273">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="30b6d-274">Une interface BITS personnalisée est utile lorsque vous fournissez un canal de distribution de contenu personnalisé autre que les canaux intégrés « Click-to-Run » tels que les CDN, les serveurs IIS ou les partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="30b6d-274">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="30b6d-275">La condition minimale requise pour qu’une interface BITS personnalisée fonctionne avec Office service C2R est :</span><span class="sxs-lookup"><span data-stu-id="30b6d-275">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="30b6d-276">Pour **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="30b6d-276">For **IBackgroundCopyManager**:</span></span>
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- <span data-ttu-id="30b6d-277">Pour **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="30b6d-277">For **IBackgroundCopyJob**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- <span data-ttu-id="30b6d-278">Pour **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="30b6d-278">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="30b6d-279">Pour les  `Addfile`  `AddFileWithRanges` fonctions, l’URL distante est au format suivant :</span><span class="sxs-lookup"><span data-stu-id="30b6d-279">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="30b6d-280">cmbits est codé en dur et signifie BITS personnalisé.</span><span class="sxs-lookup"><span data-stu-id="30b6d-280">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="30b6d-281">_\<contentid\>_ est le _paramètre contentid_ de la **méthode Download().**</span><span class="sxs-lookup"><span data-stu-id="30b6d-281">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="30b6d-282">_\<relative path to target file\>_ fournit l’emplacement et le nom du fichier à télécharger.</span><span class="sxs-lookup"><span data-stu-id="30b6d-282">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="30b6d-283">Par exemple, si vous avez fourni un _contentid_ de la méthode Download() et que Office C2R souhaite télécharger le fichier cab version, tel que le fichier, il appelle `f732af58-5d86-4299-abe9-7595c35136ef`  `v32.cab` **AddFile()** avec les informations suivantes `RemoteUrl` :</span><span class="sxs-lookup"><span data-stu-id="30b6d-283">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="30b6d-284">Pour **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="30b6d-284">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="30b6d-285">Pour **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="30b6d-285">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a><span data-ttu-id="30b6d-286">Automatisation de la zone de transit de contenu</span><span class="sxs-lookup"><span data-stu-id="30b6d-286">Automating content staging</span></span>

<span data-ttu-id="30b6d-287">Les administrateurs informatiques peuvent choisir que les clients de bureau soient activés pour recevoir automatiquement les mises à jour lorsqu’ils sont disponibles directement à partir du CDN ou ils peuvent choisir de contrôler le déploiement des mises à jour disponibles à partir des canaux de mise à jour à l’aide de l’outil déploiement Office ou de Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="30b6d-287">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the CDN or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or Microsoft Endpoint Configuration Manager.</span></span>
  
<span data-ttu-id="30b6d-288">Le service prend en charge la possibilité pour les outils de gestion de reconnaître et d’automatiser le téléchargement du contenu lorsque des mises à jour sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="30b6d-288">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="30b6d-289">**L’image suivante est une vue d’ensemble du téléchargement d’une image personnalisée**</span><span class="sxs-lookup"><span data-stu-id="30b6d-289">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="30b6d-290">![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM Office programme d’installation « Exécuter en un clic")</span><span class="sxs-lookup"><span data-stu-id="30b6d-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="30b6d-291">Vue d’ensemble du téléchargement d’une image personnalisée</span><span class="sxs-lookup"><span data-stu-id="30b6d-291">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="30b6d-292">Dans le diagramme précédent, vous voyez qu’une nouvelle image Microsoft 365 Apps est disponible sur le CDN.</span><span class="sxs-lookup"><span data-stu-id="30b6d-292">In the previous diagram, you see that a new Microsoft 365 Apps image is available on the CDN.</span></span> <span data-ttu-id="30b6d-293">Parallèlement à l’image Microsoft 365 Apps, une API est disponible et dispose des informations nécessaires pour permettre aux logiciels de gestion de créer directement des images personnalisées en remplaçant la nécessité d’utiliser l’outil déploiement Office.</span><span class="sxs-lookup"><span data-stu-id="30b6d-293">Along with the Microsoft 365 Apps image, an API is available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>

<span data-ttu-id="30b6d-294">Une entreprise configure son service WSUS pour synchroniser les mises Microsoft 365 Apps jour.</span><span class="sxs-lookup"><span data-stu-id="30b6d-294">An enterprise configures their WSUS to sync the Microsoft 365 Apps updates.</span></span> <span data-ttu-id="30b6d-295">Ces mises à jour ne contiennent pas la charge utile réelle de l’image, mais permettent au logiciel de gestion de reconnaître quand du nouveau contenu est disponible.</span><span class="sxs-lookup"><span data-stu-id="30b6d-295">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="30b6d-296">Le logiciel de gestion peut ensuite lire les Microsoft 365 Apps de mise à jour pour comprendre à quelle version Office la mise à jour s’applique.</span><span class="sxs-lookup"><span data-stu-id="30b6d-296">The manageability software can then read the Microsoft 365 Apps Update metadata to understand what version of Office the update applies to.</span></span>

<span data-ttu-id="30b6d-297">Si la mise à jour est applicable, le logiciel de gestion peut utiliser le contenu CDN et la liste de fichiers pour créer l’image personnalisée et la stocker sur l’emplacement de partage de fichiers qu’il est configuré pour utiliser.</span><span class="sxs-lookup"><span data-stu-id="30b6d-297">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a><span data-ttu-id="30b6d-298">Utilisation de l’API Microsoft 365 Apps liste de fichiers</span><span class="sxs-lookup"><span data-stu-id="30b6d-298">Using the Microsoft 365 Apps file list API</span></span>

<span data-ttu-id="30b6d-299">L Microsoft 365 Apps API de liste de fichiers est utilisée pour récupérer les noms des fichiers nécessaires à une mise à jour Microsoft 365 Apps spécifique.</span><span class="sxs-lookup"><span data-stu-id="30b6d-299">The Microsoft 365 Apps file list API is used to retrieve the names of the files needed for a particular Microsoft 365 Apps update.</span></span>

<span data-ttu-id="30b6d-300">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="30b6d-300">HTTP Request</span></span>

<span data-ttu-id="30b6d-301">GET https://config.office.com/api/filelist</span><span class="sxs-lookup"><span data-stu-id="30b6d-301">GET https://config.office.com/api/filelist</span></span>

<span data-ttu-id="30b6d-302">N’indiquez pas le corps de la demande pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="30b6d-302">Do not supply a request body for this method.</span></span>

<span data-ttu-id="30b6d-303">Aucune autorisation n’est requise pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="30b6d-303">No permissions are required to call this API.</span></span>

<span data-ttu-id="30b6d-304">Paramètres facultatifs de la requête</span><span class="sxs-lookup"><span data-stu-id="30b6d-304">Optional query parameters</span></span>

|<span data-ttu-id="30b6d-305">**Name**</span><span class="sxs-lookup"><span data-stu-id="30b6d-305">**Name**</span></span>|<span data-ttu-id="30b6d-306">**Description**</span><span class="sxs-lookup"><span data-stu-id="30b6d-306">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="30b6d-307">canal</span><span class="sxs-lookup"><span data-stu-id="30b6d-307">channel</span></span> <br/>| <span data-ttu-id="30b6d-308">Spécifie le nom du canal</span><span class="sxs-lookup"><span data-stu-id="30b6d-308">Specifies the channel name</span></span>  <br/> <span data-ttu-id="30b6d-309">Facultatif : valeur par défaut « SemiAnnual »</span><span class="sxs-lookup"><span data-stu-id="30b6d-309">Optional – default to ‘SemiAnnual’</span></span> <br/> <span data-ttu-id="30b6d-310">Valeurs pris en charge https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span><span class="sxs-lookup"><span data-stu-id="30b6d-310">Supported values https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span></span> |
| <span data-ttu-id="30b6d-311">version</span><span class="sxs-lookup"><span data-stu-id="30b6d-311">version</span></span> <br/>| <span data-ttu-id="30b6d-312">Spécifie la version de mise à jour</span><span class="sxs-lookup"><span data-stu-id="30b6d-312">Specifies the update version</span></span> <br/> <span data-ttu-id="30b6d-313">Facultatif : valeur par défaut de la dernière version disponible pour le canal spécifié</span><span class="sxs-lookup"><span data-stu-id="30b6d-313">Optional – defaults to the latest version available for the specified channel</span></span> |
| <span data-ttu-id="30b6d-314">arch</span><span class="sxs-lookup"><span data-stu-id="30b6d-314">arch</span></span> <br/>| <span data-ttu-id="30b6d-315">Spécifie l’architecture du client</span><span class="sxs-lookup"><span data-stu-id="30b6d-315">Specifies client architecture</span></span> <br/> <span data-ttu-id="30b6d-316">Facultatif : valeur par défaut de ' x64'</span><span class="sxs-lookup"><span data-stu-id="30b6d-316">Optional – defaults to ‘x64’</span></span> <br/> <span data-ttu-id="30b6d-317">Valeurs prise en charge : x64, x86</span><span class="sxs-lookup"><span data-stu-id="30b6d-317">Supported values: x64, x86</span></span> |
| <span data-ttu-id="30b6d-318">lid</span><span class="sxs-lookup"><span data-stu-id="30b6d-318">lid</span></span> <br/>| <span data-ttu-id="30b6d-319">Spécifie les fichiers de langue à inclure</span><span class="sxs-lookup"><span data-stu-id="30b6d-319">Specifies the language files to include</span></span> <br/> <span data-ttu-id="30b6d-320">Facultatif : aucune valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="30b6d-320">Optional – defaults to none</span></span> <br/> <span data-ttu-id="30b6d-321">Pour spécifier plusieurs langues, incluez un paramètre de requête de capot pour chaque langue</span><span class="sxs-lookup"><span data-stu-id="30b6d-321">To specify multiple languages, include an lid query parameter for each language</span></span> <br/> <span data-ttu-id="30b6d-322">Utilisez le format d’identificateur de langue, par exemple.</span><span class="sxs-lookup"><span data-stu-id="30b6d-322">Use the language identifier format, ex.</span></span> <span data-ttu-id="30b6d-323">'en-us', 'fr-fr'</span><span class="sxs-lookup"><span data-stu-id="30b6d-323">‘en-us’, ‘fr-fr’</span></span> |
| <span data-ttu-id="30b6d-324">alllanguages</span><span class="sxs-lookup"><span data-stu-id="30b6d-324">alllanguages</span></span> <br/>| <span data-ttu-id="30b6d-325">Spécifie d’inclure tous les fichiers de langue</span><span class="sxs-lookup"><span data-stu-id="30b6d-325">Specifies to include all language files</span></span> <br/> <span data-ttu-id="30b6d-326">Facultatif : valeurs par défaut sur false</span><span class="sxs-lookup"><span data-stu-id="30b6d-326">Optional – defaults to false</span></span> |

<span data-ttu-id="30b6d-327">Réponse HTTP</span><span class="sxs-lookup"><span data-stu-id="30b6d-327">HTTP Response</span></span>

<span data-ttu-id="30b6d-328">Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets de fichier dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="30b6d-328">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="30b6d-329">Pour créer une image, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="30b6d-329">To create an image, follow these steps:</span></span>
1.  <span data-ttu-id="30b6d-330">Appelez l’API, en fournissant les paramètres de requête appropriés pour le canal, la version et l’architecture de la mise à jour qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="30b6d-330">Call the API, providing the appropriate query parameters for the channel, version and architecture of the update you are interested in.</span></span>
<span data-ttu-id="30b6d-331">Remarque : les objets de fichier avec l’attribut « lcid » : « 0 » sont des fichiers linguistiquement neutres et doivent être inclus dans l’image.</span><span class="sxs-lookup"><span data-stu-id="30b6d-331">Note: File objects with the attribute "lcid": "0" are language neutral files and must be included in the image.</span></span>
2.  <span data-ttu-id="30b6d-332">Créez une image locale du CDN en itérant les objets de fichier et en copiant les fichiers CDN, tout en créant la structure de dossiers spécifiée par l’attribut « relativePath » défini pour chacun des objets de fichier.</span><span class="sxs-lookup"><span data-stu-id="30b6d-332">Construct a local image of the CDN by iterating through the file objects and copying the CDN files, while creating the folder structure as specified by the “relativePath” attribute defined for each of the file objects.</span></span>

<span data-ttu-id="30b6d-333">L’exemple suivant récupère la liste des fichiers pour le canal actuel et la version 16.0.4229.1004 pour 64 bits et inclut les fichiers en français et en anglais :</span><span class="sxs-lookup"><span data-stu-id="30b6d-333">The following example retrieves the file list for the Current Channel and version 16.0.4229.1004 for 64bit and includes the French and English language files:</span></span>

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="30b6d-334">Vérification de hachage des fichiers .dat</span><span class="sxs-lookup"><span data-stu-id="30b6d-334">Hash verification of .dat files</span></span>

<span data-ttu-id="30b6d-335">Les outils de création d’images peuvent vérifier l’intégrité des fichiers .dat téléchargés en comparant une valeur de hachage calculée à la valeur de hachage fournie associée à chacun des fichiers .dat.</span><span class="sxs-lookup"><span data-stu-id="30b6d-335">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed hash value with the supplied hash value associated with each of the .dat files.</span></span> <span data-ttu-id="30b6d-336">Voici un exemple d’objet fichier qui spécifie les valeurs hashLocation et hashAlgorithm :</span><span class="sxs-lookup"><span data-stu-id="30b6d-336">Following is an example of a file object that specifies hashLocation and hashAlgorithm values:</span></span>
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- <span data-ttu-id="30b6d-337">**L’attribut hashLocation** spécifie l’emplacement du chemin d’accès relatif .cab fichier contenant la valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="30b6d-337">The **hashLocation** attribute specifies the relative path location of .cab file that contains the hash value.</span></span> <span data-ttu-id="30b6d-338">Construisez l’emplacement du fichier de hachage en concatenant l’URL + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="30b6d-338">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="30b6d-339">Dans l’exemple suivant, l stream.x64.bg-bg.hash serait :</span><span class="sxs-lookup"><span data-stu-id="30b6d-339">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="30b6d-340">**L’attribut hashAlgorithm** spécifie l’algorithme de hachage utilisé.</span><span class="sxs-lookup"><span data-stu-id="30b6d-340">The **hashAlgorithm** attribute specifies what hashing algorithm was used.</span></span> 
    
  <span data-ttu-id="30b6d-341">Pour valider l’intégrité du fichier stream.x64.bg-bg.dat, ouvrez le fichier stream.x64.bg-bg.hash et lisez la valeur HASH qui est la première ligne de texte du fichier de hachage.</span><span class="sxs-lookup"><span data-stu-id="30b6d-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="30b6d-342">Comparez cette valeur à la valeur de hachage calculée (à l’aide de l’algorithme de hachage spécifié) pour vérifier l’intégrité du fichier .dat téléchargé.</span><span class="sxs-lookup"><span data-stu-id="30b6d-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="30b6d-343">L’exemple suivant montre comment C# code pour lire le hachage.</span><span class="sxs-lookup"><span data-stu-id="30b6d-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a><span data-ttu-id="30b6d-344">Microsoft 365 Apps Mises à jour</span><span class="sxs-lookup"><span data-stu-id="30b6d-344">Microsoft 365 Apps Updates</span></span>

<span data-ttu-id="30b6d-345">Toutes Microsoft 365 Apps mises à jour sont publiées dans le [catalogue Microsoft Update.](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)</span><span class="sxs-lookup"><span data-stu-id="30b6d-345">All Microsoft 365 Apps Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="30b6d-346">Microsoft 365 Apps Les mises à jour permettent aux logiciels de gestion de traiter Microsoft 365 Apps mises à jour d’une manière très similaire à toute autre mise à jour WU, à une exception près . les mises à jour du client ne contiennent pas de charge utile réelle.</span><span class="sxs-lookup"><span data-stu-id="30b6d-346">Microsoft 365 Apps Updates enable manageability software to treat Microsoft 365 Apps Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="30b6d-347">Les mises à jour Microsoft 365 Apps ne doivent pas être installées sur les clients, mais plutôt utilisées pour déclencher les flux de travail avec le logiciel de gestion remplaçant la commande d’installation par le mécanisme d’installation COM indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="30b6d-347">The Microsoft 365 Apps Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span>

<span data-ttu-id="30b6d-348">**La figure suivante montre un diagramme du flux de travail Office 365 de mise à jour du client.**</span><span class="sxs-lookup"><span data-stu-id="30b6d-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="30b6d-349">![Diagramme de flux de travail pour les mises à jour du client O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagramme de flux de travail pour les mises à jour du client O365PP")</span><span class="sxs-lookup"><span data-stu-id="30b6d-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="30b6d-350">Chaque Microsoft 365 Apps mise à jour publiée inclut des métadonnées sur la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="30b6d-350">Each Microsoft 365 Apps Update that is published includes metadata about the update.</span></span> <span data-ttu-id="30b6d-351">Ces métadonnées incluent un paramètre appelé MoreInfoUrl qui peut être utilisé pour dériver l’appel d’API à l’API de liste de fichiers pour cette mise à jour spécifique.</span><span class="sxs-lookup"><span data-stu-id="30b6d-351">This metadata includes a parameter called MoreInfoUrl which can be used to derive the API call to the file list API for that specific update.</span></span>

<span data-ttu-id="30b6d-352">Dans l’exemple suivant, l’API de liste de fichiers est incorporée dans moreInfoURL et commence par « ServicePath= »</span><span class="sxs-lookup"><span data-stu-id="30b6d-352">In the following example, the file list API is embedded in the MoreInfoURL and starts with “ServicePath=”</span></span>

<span data-ttu-id="30b6d-353"> http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span><span class="sxs-lookup"><span data-stu-id="30b6d-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span></span>
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="30b6d-354">Métadonnées supplémentaires pour l’automatisation de la zone de transit de contenu</span><span class="sxs-lookup"><span data-stu-id="30b6d-354">Additional metadata for automating content staging</span></span>

<span data-ttu-id="30b6d-355">**API d’historique des sorties**</span><span class="sxs-lookup"><span data-stu-id="30b6d-355">**Release History API**</span></span>
  
<span data-ttu-id="30b6d-356">L Microsoft 365 Apps’API d’historique des mises à jour est utilisée pour récupérer les détails de chacune des mises à jour publiées sur le CDN avec les noms de canaux et d’autres attributs de canal.</span><span class="sxs-lookup"><span data-stu-id="30b6d-356">The Microsoft 365 Apps release history API is used to retrieve details for each of the updates published to the CDN along with the channel names and other channel attributes.</span></span>

<span data-ttu-id="30b6d-357">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="30b6d-357">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/channels 
```

<span data-ttu-id="30b6d-358">N’indiquez pas le corps de la demande pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="30b6d-358">Do not supply a request body for this method.</span></span>

<span data-ttu-id="30b6d-359">Aucune autorisation n’est requise pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="30b6d-359">No permissions are required to call this API.</span></span>

<span data-ttu-id="30b6d-360">Réponse HTTP</span><span class="sxs-lookup"><span data-stu-id="30b6d-360">HTTP Response</span></span>

<span data-ttu-id="30b6d-361">Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets de fichier dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="30b6d-361">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="30b6d-362">**SKUs API**</span><span class="sxs-lookup"><span data-stu-id="30b6d-362">**SKUs API**</span></span>
  
<span data-ttu-id="30b6d-363">L’API SSK retourne des informations utiles pour déterminer les produits disponibles pour le déploiement et la maintenance à partir du Office CDN avec différentes options pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="30b6d-363">The SKUs API returns information that is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span>

<span data-ttu-id="30b6d-364">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="30b6d-364">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/skus 
```

<span data-ttu-id="30b6d-365">N’indiquez pas le corps de la demande pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="30b6d-365">Do not supply a request body for this method.</span></span>

<span data-ttu-id="30b6d-366">Aucune autorisation n’est requise pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="30b6d-366">No permissions are required to call this API.</span></span>

<span data-ttu-id="30b6d-367">Réponse HTTP</span><span class="sxs-lookup"><span data-stu-id="30b6d-367">HTTP Response</span></span>

<span data-ttu-id="30b6d-368">Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets de fichier dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="30b6d-368">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>
