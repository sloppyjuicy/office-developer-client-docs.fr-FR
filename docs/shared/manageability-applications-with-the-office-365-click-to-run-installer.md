---
title: Intégration des applications de gestion avec les applications Microsoft 365 installer le programme d’installation « démarrer en un clic »
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Découvrez comment intégrer le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 avec une solution de gestion de logiciels.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297313"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a><span data-ttu-id="5dd28-103">Intégration des applications de gestion avec les applications Microsoft 365 installer le programme d’installation « démarrer en un clic »</span><span class="sxs-lookup"><span data-stu-id="5dd28-103">Integrating manageability applications with Microsoft 365 Apps Click-to-Run installer</span></span>

<span data-ttu-id="5dd28-104">Découvrez comment intégrer le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 avec une solution de gestion de logiciels.</span><span class="sxs-lookup"><span data-stu-id="5dd28-104">Learn how to integrate the Microsoft 365 Apps Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="5dd28-105">Le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 fournit une interface COM qui permet aux professionnels de l’informatique et au contrôle par programme des solutions de gestion des logiciels de gérer les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="5dd28-105">The Microsoft 365 Apps Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="5dd28-106">Cette interface fournit des fonctionnalités de gestion supplémentaires au-delà de ce qui est fourni par l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="5dd28-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5dd28-107">Cet article s’applique aux applications Office qui utilisent le programme d’installation « démarrer en un clic ».</span><span class="sxs-lookup"><span data-stu-id="5dd28-107">This article applies to Office apps that use the Click-to-Run installer.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="5dd28-108">Intégration à « démarrer en un clic »</span><span class="sxs-lookup"><span data-stu-id="5dd28-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="5dd28-109">Pour utiliser cette interface, une application de gérabilité appelle l’interface COM et appelle des API exposées qui communiquent directement avec le service d’installation « démarrer en un clic ».</span><span class="sxs-lookup"><span data-stu-id="5dd28-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5dd28-110">Le programme d’installation Office « démarrer en un clic » peut être exécuté à partir de la ligne de commande avec des paramètres qui peuvent contrôler le comportement, comme indiqué dans l' [outil déploiement d’Office pour démarrer en un clic](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span><span class="sxs-lookup"><span data-stu-id="5dd28-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span></span> 
  
<span data-ttu-id="5dd28-111">**Voici un diagramme conceptuel de l’interface COM**</span><span class="sxs-lookup"><span data-stu-id="5dd28-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="5dd28-112">![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM sur le programme d’installation Office « démarrer en un clic »")</span><span class="sxs-lookup"><span data-stu-id="5dd28-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="5dd28-113">Le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 implémente une interface COM, **IUpdateNotify** inscrite au CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="5dd28-113">The Microsoft 365 Apps Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="5dd28-114">Cette interface peut être appelée comme suit :</span><span class="sxs-lookup"><span data-stu-id="5dd28-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="5dd28-115">L’appel ne réussira que si l’appelant s’exécute sous des privilèges élevés, car le programme d’installation démarrer en un clic doit être exécuté avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="5dd28-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="5dd28-116">L’interface com **IUpdateNotify** expose trois fonctions asynchrones chargées de la validation des commandes et des paramètres et de l’exécution de la planification avec le service d’installation « démarrer en un clic ».</span><span class="sxs-lookup"><span data-stu-id="5dd28-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="5dd28-117">Une méthode, **Status**, peut être utilisée pour obtenir des informations sur l’état de la dernière commande exécutée ou l’état de la commande en cours d’exécution (c.-à-d. réussite, échec, codes d’erreur détaillés).</span><span class="sxs-lookup"><span data-stu-id="5dd28-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="5dd28-118">Il existe quatre États selon lesquels le service d’installation « démarrer en un clic » peut se trouver pendant son cycle de vie, pendant laquelle les méthodes **IUpdateNotify** peuvent être appelées ; Redémarrage, inactivité, téléchargement et application.</span><span class="sxs-lookup"><span data-stu-id="5dd28-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="5dd28-119">**Le schéma de machine à États de l’interface COM est le suivant :**</span><span class="sxs-lookup"><span data-stu-id="5dd28-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="5dd28-120">![Diagramme d’état pour l’interface COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Diagramme d’État pour l’interface COM")</span><span class="sxs-lookup"><span data-stu-id="5dd28-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="5dd28-121">**Redémarrage**: lors du démarrage de l’ordinateur, le service d’installation « démarrer en un clic » n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="5dd28-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="5dd28-122">Un appel réussi à la méthode Status après un redémarrage renverra eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="5dd28-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="5dd28-123">**Inactif :** Lorsque le programme d’installation « démarrer en un clic » est à l’état inactif, vous pouvez appeler les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5dd28-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="5dd28-124">**Appliquer**: installer le contenu précédemment téléchargé.</span><span class="sxs-lookup"><span data-stu-id="5dd28-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="5dd28-125">**Cancel**: renvoie  `0x800000e` , « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="5dd28-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="5dd28-126">**Téléchargement**: télécharge le nouveau contenu sur le client pour une installation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5dd28-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="5dd28-127">**État**: renvoie le résultat de la dernière action terminée ou un message d’erreur si l’action s’est terminée en raison d’un échec.</span><span class="sxs-lookup"><span data-stu-id="5dd28-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="5dd28-128">S’il n’existe aucune action précédente, **Status** renvoie  `eUPDATE_UNKNOWN` .</span><span class="sxs-lookup"><span data-stu-id="5dd28-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="5dd28-129">**Téléchargement :** Lorsque le programme d’installation démarrer en un clic est à l’état de téléchargement, vous pouvez appeler les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5dd28-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="5dd28-130">**Apply**: retourne un **HRESULT** avec la valeur  `0x800000e` « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="5dd28-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="5dd28-131">**Cancel**: arrête le téléchargement et supprime le contenu partiellement téléchargé.</span><span class="sxs-lookup"><span data-stu-id="5dd28-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="5dd28-132">**Téléchargement**: retourne un **HRESULT** avec la valeur  `0x800000e` « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="5dd28-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="5dd28-133">**Status**: renvoie **DOWNLOAD_WIP** pour indiquer que le téléchargement est en cours.</span><span class="sxs-lookup"><span data-stu-id="5dd28-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="5dd28-134">**Application :** Lorsque le programme d’installation « démarrer en un clic » se trouve dans le processus d’installation du contenu précédemment téléchargé :</span><span class="sxs-lookup"><span data-stu-id="5dd28-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="5dd28-135">**Apply**: retourne un **HRESULT** avec la valeur  `0x800000e` « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="5dd28-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="5dd28-136">**Cancel**: renvoie  `0x800000e` , l’action Apply ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="5dd28-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="5dd28-137">**Téléchargement**: retourne un **HRESULT** avec la valeur  `0x800000e` « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="5dd28-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="5dd28-138">**État**: renvoie **APPLY_WIP** pour indiquer que l’opération d’application est en cours.</span><span class="sxs-lookup"><span data-stu-id="5dd28-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="5dd28-139">Étant donné que OfficeC2RCOM est un service COM+ et qu’il est chargé dynamiquement, vous devez appeler **CoCreateInstance** chaque fois que vous appelez une méthode sur cette classe afin de vous assurer que vous obtenez le résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="5dd28-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="5dd28-140">Le service COM+ gère la création d’une nouvelle instance si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5dd28-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="5dd28-141">Lorsqu’une des méthodes est appelée pour la première fois, COM+ charge l’objet **IUpdateNotify** et l’exécute dans l’une des instances dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="5dd28-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="5dd28-142">Le nouvel objet reste actif pendant environ 3 minutes d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="5dd28-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="5dd28-143">Si un appel est effectué dans les trois minutes suivant le dernier appel, l’objet **IUpdateNotify** reste chargé et une nouvelle instance n’est pas créée.</span><span class="sxs-lookup"><span data-stu-id="5dd28-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="5dd28-144">Si aucun appel n’est effectué dans les trois minutes, l’objet IUpdateNotify est déchargé et un nouvel objet **IUpdateNotify** est créé lors de l’appel suivant.</span><span class="sxs-lookup"><span data-stu-id="5dd28-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="5dd28-145">Guide de référence de l’API COM « démarrer en un clic »</span><span class="sxs-lookup"><span data-stu-id="5dd28-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="5dd28-146">Dans la documentation de référence de l’API suivante :</span><span class="sxs-lookup"><span data-stu-id="5dd28-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="5dd28-147">Les paramètres se trouvent dans un format de paire clé/valeur séparé par un espace.</span><span class="sxs-lookup"><span data-stu-id="5dd28-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="5dd28-148">Les paramètres ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="5dd28-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="5dd28-149">Il existe une [liste de paramètres](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) avec la documentation disponible.</span><span class="sxs-lookup"><span data-stu-id="5dd28-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="5dd28-150">Le résumé de l’interface IUpdateNotify2 est désormais inclus.</span><span class="sxs-lookup"><span data-stu-id="5dd28-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="5dd28-151">Appliquer</span><span class="sxs-lookup"><span data-stu-id="5dd28-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="5dd28-152">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dd28-152">Parameters</span></span>

-  <span data-ttu-id="5dd28-153">_DisplayLevel_: **true** pour afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false** pour masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5dd28-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="5dd28-154">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="5dd28-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="5dd28-155">_forceappshutdown_: **true** pour obliger les applications Office à s’arrêter immédiatement lorsque l’action d' **application** est déclenchée ; **false** pour faire échouer si des applications Office sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5dd28-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="5dd28-156">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="5dd28-156">The default is **false**.</span></span> <span data-ttu-id="5dd28-157">Pour plus d’informations, voir [Remarques](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="5dd28-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="5dd28-158">Si une application Office est en cours d’exécution lorsque l’action d' **application** est déclenchée **, l’action d’application échoue** généralement.</span><span class="sxs-lookup"><span data-stu-id="5dd28-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="5dd28-159">`forceappshutdown=true`En passant à la méthode **apply** , le service **OfficeClickToRun** arrête immédiatement les applications et applique la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5dd28-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="5dd28-160">Dans ce cas, l’utilisateur peut subir une perte de données.</span><span class="sxs-lookup"><span data-stu-id="5dd28-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="5dd28-161">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="5dd28-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dd28-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="5dd28-162">**S_OK**</span></span> <br/> |<span data-ttu-id="5dd28-163">L’action a été correctement envoyée au service « démarrer en un clic » pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5dd28-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="5dd28-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="5dd28-165">L’appelant n’est pas en cours d’exécution avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="5dd28-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="5dd28-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="5dd28-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="5dd28-167">Les paramètres non valides ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="5dd28-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="5dd28-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="5dd28-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="5dd28-169">L’action n’est pas autorisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="5dd28-169">Action is not allowed at this time.</span></span> <span data-ttu-id="5dd28-170">Pour plus d’informations, voir [Remarques](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="5dd28-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="5dd28-171">Remarques</span><span class="sxs-lookup"><span data-stu-id="5dd28-171">Remarks</span></span>

- <span data-ttu-id="5dd28-172">Si une application Office est en cours d’exécution lorsque l’action d' **application** est déclenchée **, l’action d’application échoue** .</span><span class="sxs-lookup"><span data-stu-id="5dd28-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="5dd28-173">`forceappshutdown=true`En passant à la méthode **apply** , le service **OfficeClickToRun** arrête immédiatement toutes les applications Office en cours d’exécution et applique la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5dd28-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="5dd28-174">L’utilisateur peut se servir des données, car il n’est pas invité à enregistrer les modifications apportées aux documents ouverts..</span><span class="sxs-lookup"><span data-stu-id="5dd28-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="5dd28-175">Cette action ne peut être déclenchée que lorsque le statut COM est l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="5dd28-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="5dd28-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="5dd28-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="5dd28-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="5dd28-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="5dd28-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="5dd28-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="5dd28-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="5dd28-182">Si vous appelez la méthode **apply** sans télécharger le contenu précédemment, la méthode **apply** signalera la **réussite** car elle n’a pas pu s’appliquer et a terminé le processus d' **application** .</span><span class="sxs-lookup"><span data-stu-id="5dd28-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="5dd28-183">Annuler</span><span class="sxs-lookup"><span data-stu-id="5dd28-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="5dd28-184">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="5dd28-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dd28-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="5dd28-185">S_OK</span></span>  <br/> |<span data-ttu-id="5dd28-186">L’action a été correctement envoyée au service « démarrer en un clic » pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5dd28-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="5dd28-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="5dd28-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="5dd28-188">L’action n’est pas autorisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="5dd28-188">Action is not allowed at this time.</span></span> <span data-ttu-id="5dd28-189">Pour plus d’informations, consultez la section [Remarques](#bk_CancelRemarks) .</span><span class="sxs-lookup"><span data-stu-id="5dd28-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="5dd28-190">Remarques</span><span class="sxs-lookup"><span data-stu-id="5dd28-190">Remarks</span></span>

- <span data-ttu-id="5dd28-191">Cette méthode ne peut être déclenchée que lorsque l’ID d’État COM **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="5dd28-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="5dd28-192">Elle tentera d’annuler l’action de téléchargement en cours.</span><span class="sxs-lookup"><span data-stu-id="5dd28-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="5dd28-193">L’état de COM passe à **eDOWNLOAD_CANCELLING** et change finalement en **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="5dd28-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="5dd28-194">L’État COM renvoie **E_ILLEGAL_METHOD_CALL** s’il est déclenché à tout autre moment.</span><span class="sxs-lookup"><span data-stu-id="5dd28-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="5dd28-195">Télécharger</span><span class="sxs-lookup"><span data-stu-id="5dd28-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="5dd28-196">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dd28-196">Parameters</span></span>

-  <span data-ttu-id="5dd28-197">_DisplayLevel_: **true** pour afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false** pour masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5dd28-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="5dd28-198">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="5dd28-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="5dd28-199">_updatebaseurl_: URL vers l’autre source de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="5dd28-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="5dd28-200">_updatetoversion_: version à mettre à jour Office vers.</span><span class="sxs-lookup"><span data-stu-id="5dd28-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="5dd28-201">Définissez ce paramètre si vous souhaitez effectuer une mise à jour vers une version antérieure à la version actuellement installée.</span><span class="sxs-lookup"><span data-stu-id="5dd28-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="5dd28-202">_downloadsource_: CLSID de l’implémentation **IBackgroundCopyManager** personnalisée (gestionnaire bits).</span><span class="sxs-lookup"><span data-stu-id="5dd28-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="5dd28-203">_contentid_: identifie le contenu à télécharger à partir du serveur de contenu via le gestionnaire des bits personnalisé.</span><span class="sxs-lookup"><span data-stu-id="5dd28-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="5dd28-204">Cette valeur est transmise à l’interprétation via l’interface BITS.</span><span class="sxs-lookup"><span data-stu-id="5dd28-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="5dd28-205">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="5dd28-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dd28-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="5dd28-206">**S_OK**</span></span> <br/> |<span data-ttu-id="5dd28-207">L’action a été correctement envoyée au service « démarrer en un clic » pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5dd28-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="5dd28-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="5dd28-209">L’appelant n’est pas en cours d’exécution avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="5dd28-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="5dd28-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="5dd28-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="5dd28-211">Les paramètres non valides ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="5dd28-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="5dd28-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="5dd28-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="5dd28-213">L’action n’est pas autorisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="5dd28-213">Action is not allowed at this time.</span></span> <span data-ttu-id="5dd28-214">Pour plus d’informations, voir [Remarques](#bk_DownloadRemark) .</span><span class="sxs-lookup"><span data-stu-id="5dd28-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="5dd28-215">Remarques</span><span class="sxs-lookup"><span data-stu-id="5dd28-215">Remarks</span></span>

- <span data-ttu-id="5dd28-216">Vous devez spécifier  _downloadsource_ et  _contentid_ en tant que paire.</span><span class="sxs-lookup"><span data-stu-id="5dd28-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="5dd28-217">Si ce n’est pas le cas, la méthode de **Téléchargement** renvoie une erreur **E_INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="5dd28-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="5dd28-218">Si  _downloadsource_,  _contentid_et  _updatebaseurl_ sont fournis,  _updatebaseurl_ sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="5dd28-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="5dd28-219">Cette action ne peut être déclenchée que lorsque le statut COM est l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="5dd28-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="5dd28-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="5dd28-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="5dd28-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="5dd28-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="5dd28-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="5dd28-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="5dd28-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="5dd28-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="5dd28-226">Si vous appelez la méthode **apply** sans le contenu précédemment téléchargé, la méthode **apply** signalera la **réussite** car elle n’a pas pu s’appliquer et a terminé le processus d' **application** .</span><span class="sxs-lookup"><span data-stu-id="5dd28-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="5dd28-227">Exemples</span><span class="sxs-lookup"><span data-stu-id="5dd28-227">Examples</span></span>

- <span data-ttu-id="5dd28-228">Pour télécharger le contenu à partir du gestionnaire des fichiers BITS personnalisé : appelez la fonction **Download ()** en transmettant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="5dd28-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="5dd28-229">Pour télécharger le contenu à partir du réseau de distribution de contenu (CDN) Office : appelez la fonction **Download ()** sans spécifier les paramètres  _downloadsource_,  _contentid_ou  _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="5dd28-229">To download the content from the Office Content Delivery Network (CDN): Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="5dd28-230">Pour télécharger le contenu à partir d’un emplacement personnalisé : appelez la fonction **Download ()** en transmettant le paramètre suivant :</span><span class="sxs-lookup"><span data-stu-id="5dd28-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="5dd28-231">Statut</span><span class="sxs-lookup"><span data-stu-id="5dd28-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="5dd28-232">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dd28-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="5dd28-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="5dd28-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="5dd28-234">Pointeur vers une structure UPDATE_STATUS_REPORT.</span><span class="sxs-lookup"><span data-stu-id="5dd28-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="5dd28-235">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="5dd28-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dd28-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="5dd28-236">**S_OK**</span></span> <br/> |<span data-ttu-id="5dd28-237">La méthode **Status** renvoie toujours ce résultat.</span><span class="sxs-lookup"><span data-stu-id="5dd28-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="5dd28-238">Inspectez la  `UPDATE_STATUS_RESULT` structure pour connaître l’état de l’action actuelle.</span><span class="sxs-lookup"><span data-stu-id="5dd28-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="5dd28-239">Remarques</span><span class="sxs-lookup"><span data-stu-id="5dd28-239">Remarks</span></span>

- <span data-ttu-id="5dd28-240">Champ d’état de la  `UPDATE_STATUS_REPORT` contient l’état de l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="5dd28-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="5dd28-241">L’une des valeurs d’État suivantes est renvoyée :</span><span class="sxs-lookup"><span data-stu-id="5dd28-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="5dd28-242">Si la dernière commande a généré une erreur, le champ d’erreur de  `UPDATE_STATUS_REPORT` contient des informations détaillées sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="5dd28-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="5dd28-243">Deux types de codes d’erreur sont renvoyés à partir de la méthode **Status** .</span><span class="sxs-lookup"><span data-stu-id="5dd28-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="5dd28-244">Si l’erreur est inférieure à  `UPDATE_ERROR_CODE::eUNKNOWN` , l’erreur est l’un des codes d’erreur prédéfinis suivants :</span><span class="sxs-lookup"><span data-stu-id="5dd28-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="5dd28-245">Si le code d’erreur renvoyé est plus grand que  `UPDATE_ERROR_CODE::eUNKNOWN` le **HRESULT** d’un appel de fonction ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="5dd28-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="5dd28-246">Pour extraire la soustraction HRESULT  `UPDATE_ERROR_CODE::eUNKNOWN` de la valeur renvoyée dans le champ Error du  `UPDATE_STATUS_REPORT` .</span><span class="sxs-lookup"><span data-stu-id="5dd28-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="5dd28-247">La liste complète des valeurs d’État et d’erreur peut être affichée en inspectant la bibliothèque de types **IUpdateNotify** incorporée dans OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="5dd28-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="5dd28-248">Le champ contentid est utilisé pour les appels à l' **État** après le **Téléchargement** et renvoie le contentid qui a été transmis à l’appel de **Téléchargement** .</span><span class="sxs-lookup"><span data-stu-id="5dd28-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="5dd28-249">Il est recommandé d’initialiser ce champ sur **null** avant d’appeler la méthode **Status** , puis de vérifier la valeur après que **Status** a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="5dd28-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="5dd28-250">Si la valeur est toujours **null**, cela signifie qu’il n’existe aucun contentid à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="5dd28-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="5dd28-251">Si la valeur n’est pas **null**, vous devez la libérer avec un appel à **SysFreeString ()**.</span><span class="sxs-lookup"><span data-stu-id="5dd28-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="5dd28-252">Voici un extrait de code expliquant comment appeler l' **État** après le **Téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="5dd28-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="5dd28-253">Résumé de l’interface IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="5dd28-253">Summary of IUpdateNotify2 interface</span></span>

<span data-ttu-id="5dd28-254">À partir de la version [16.0.8208.6352] nous avons ajouté une nouvelle interface **IUpdateNotify2** .</span><span class="sxs-lookup"><span data-stu-id="5dd28-254">From version [16.0.8208.6352] we have added a new **IUpdateNotify2** interface.</span></span> 
  
- <span data-ttu-id="5dd28-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="5dd28-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="5dd28-256">Cette interface hébergeait également l’interface IUpdateNotify d’origine pour assurer la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="5dd28-256">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="5dd28-257">Cela signifie que si vous utilisez cette interface, vous avez accès à toutes les méthodes fournies dans l’interface **UpdateNotifyObject** .</span><span class="sxs-lookup"><span data-stu-id="5dd28-257">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="5dd28-258">Nouvelles méthodes ajoutées à IUpdateNotify2 :</span><span class="sxs-lookup"><span data-stu-id="5dd28-258">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="5dd28-259">**HRESULT** GetBlockingApps ([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="5dd28-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="5dd28-260">Obtenir la liste des applications de blocage des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="5dd28-260">Get updates blocking apps list.</span></span> <span data-ttu-id="5dd28-261">Cet appel renverra les applications Office en cours d’exécution, ce qui bloquera le processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5dd28-261">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="5dd28-262">**HRESULT** GetOfficeDeploymentData ([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="5dd28-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="5dd28-263">Obtenir les données de déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="5dd28-263">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="5dd28-264">Si vous souhaitez utiliser les nouvelles méthodes, vous devez vous assurer que :</span><span class="sxs-lookup"><span data-stu-id="5dd28-264">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="5dd28-265">Votre version d’C2R est plus récente que la build ci-dessus (version de la partie \> juin).</span><span class="sxs-lookup"><span data-stu-id="5dd28-265">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="5dd28-266">Utilisez UpdateNotifyObject2 au lieu de **UpdateNotifyObject** pour appeler **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="5dd28-266">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="5dd28-267">Si vous n’utilisez aucune des nouvelles méthodes, vous n’avez pas besoin de modifier quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="5dd28-267">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="5dd28-268">Toutes les méthodes existantes fonctionneront exactement de la même manière qu’avant.</span><span class="sxs-lookup"><span data-stu-id="5dd28-268">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="5dd28-269">Implémentation de l’interface BITS</span><span class="sxs-lookup"><span data-stu-id="5dd28-269">Implementing the BITS interface</span></span>

<span data-ttu-id="5dd28-270">Le [service de transfert intelligent en arrière-plan](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (bits) est un service fourni par Microsoft pour transférer des fichiers entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="5dd28-270">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="5dd28-271">BITS est l’un des canaux que le programme d’installation d’Office « démarrer en un clic » peut utiliser pour télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="5dd28-271">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="5dd28-272">Par défaut, le programme d’installation « démarrer en un clic » pour les applications Microsoft 365 utilise l’implémentation intégrée de Windows BITS pour télécharger le contenu à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="5dd28-272">By default, the Microsoft 365 Apps Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="5dd28-273">En fournissant une implémentation BITS personnalisée à la méthode de **téléchargement ()** de l’interface **IUpdateNotify** , votre logiciel de gestion peut contrôler l’emplacement et la façon dont le client télécharge le contenu.</span><span class="sxs-lookup"><span data-stu-id="5dd28-273">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="5dd28-274">Une interface BITS personnalisée est utile lorsque vous fournissez un canal de distribution de contenu personnalisé autre que les canaux intégrés « démarrer en un clic », tels que le CDN, les serveurs IIS ou les partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5dd28-274">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="5dd28-275">La configuration minimale requise pour une interface BITS personnalisée pour fonctionner avec le service Office C2R est la suivante :</span><span class="sxs-lookup"><span data-stu-id="5dd28-275">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="5dd28-276">Pour **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="5dd28-276">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="5dd28-277">Pour **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="5dd28-277">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="5dd28-278">Pour **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="5dd28-278">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="5dd28-279">Pour les  `Addfile`  `AddFileWithRanges` fonctions et, l’URL distante est au format suivant :</span><span class="sxs-lookup"><span data-stu-id="5dd28-279">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="5dd28-280">cmbits est codé en dur et représente des BITS personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5dd28-280">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="5dd28-281">_\<contentid\>_ est le paramètre  _contentid_ de la méthode **Download ()** .</span><span class="sxs-lookup"><span data-stu-id="5dd28-281">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="5dd28-282">_\<relative path to target file\>_ indique l’emplacement et le nom de fichier du fichier à télécharger.</span><span class="sxs-lookup"><span data-stu-id="5dd28-282">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="5dd28-283">Par exemple, si vous avez fourni un  _contentid_ de  `f732af58-5d86-4299-abe9-7595c35136ef` à la méthode **Download ()** et que Office C2R souhaite télécharger le fichier CAB de la version, par exemple  `v32.cab` fichier, il appellera **AddFile ()** avec les éléments suivants  `RemoteUrl` :</span><span class="sxs-lookup"><span data-stu-id="5dd28-283">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="5dd28-284">Pour **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="5dd28-284">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="5dd28-285">Pour **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="5dd28-285">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a><span data-ttu-id="5dd28-286">Automatisation du transfert de contenu</span><span class="sxs-lookup"><span data-stu-id="5dd28-286">Automating content staging</span></span>

<span data-ttu-id="5dd28-287">Les administrateurs informatiques peuvent choisir d’activer la réception automatique des mises à jour lorsqu’elles sont disponibles directement à partir du CDN ou de contrôler le déploiement des mises à jour disponibles à partir des canaux de mise à jour à l’aide de l’outil déploiement d’Office ou du gestionnaire de configuration de point de terminaison Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5dd28-287">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the CDN or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or Microsoft Endpoint Configuration Manager.</span></span>
  
<span data-ttu-id="5dd28-288">Le service prend en charge la possibilité pour les outils de gestion de reconnaître et d’automatiser le téléchargement du contenu lorsque des mises à jour sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="5dd28-288">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="5dd28-289">**L’image suivante est une vue d’ensemble du téléchargement d’une image personnalisée**</span><span class="sxs-lookup"><span data-stu-id="5dd28-289">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="5dd28-290">![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM sur le programme d’installation Office « démarrer en un clic »")</span><span class="sxs-lookup"><span data-stu-id="5dd28-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="5dd28-291">Vue d’ensemble du téléchargement d’une image personnalisée</span><span class="sxs-lookup"><span data-stu-id="5dd28-291">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="5dd28-292">Dans le schéma précédent, vous voyez qu’une nouvelle image de Microsoft 365 Apps est disponible sur le CDN.</span><span class="sxs-lookup"><span data-stu-id="5dd28-292">In the previous diagram, you see that a new Microsoft 365 Apps image is available on the CDN.</span></span> <span data-ttu-id="5dd28-293">En plus de l’image des applications Microsoft 365, une API est disponible, qui contient les informations nécessaires pour permettre aux logiciels de gestion de créer directement des images personnalisées, qui remplacent la nécessité d’utiliser l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="5dd28-293">Along with the Microsoft 365 Apps image, an API is available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>

<span data-ttu-id="5dd28-294">Une entreprise configure ses services WSUS pour synchroniser les mises à jour des applications Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5dd28-294">An enterprise configures their WSUS to sync the Microsoft 365 Apps updates.</span></span> <span data-ttu-id="5dd28-295">Ces mises à jour ne contiennent pas la charge utile de l’image réelle, mais elles permettent au logiciel de gérabilité de reconnaître quand un nouveau contenu est disponible.</span><span class="sxs-lookup"><span data-stu-id="5dd28-295">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="5dd28-296">Le logiciel de gestion peut ensuite lire les métadonnées de mise à jour des applications Microsoft 365 pour comprendre la version d’Office à laquelle la mise à jour s’applique.</span><span class="sxs-lookup"><span data-stu-id="5dd28-296">The manageability software can then read the Microsoft 365 Apps Update metadata to understand what version of Office the update applies to.</span></span>

<span data-ttu-id="5dd28-297">Si la mise à jour est applicable, le logiciel de gestion peut utiliser le contenu CDN et la liste des fichiers pour créer l’image personnalisée et la stocker sur l’emplacement de partage de fichiers qu’elle est configurée à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5dd28-297">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a><span data-ttu-id="5dd28-298">Utilisation de l’API de liste de fichiers Apps 365 Microsoft</span><span class="sxs-lookup"><span data-stu-id="5dd28-298">Using the Microsoft 365 Apps file list API</span></span>

<span data-ttu-id="5dd28-299">L’API de liste de fichiers Apps Microsoft 365 est utilisée pour récupérer les noms des fichiers nécessaires pour une mise à jour d’applications Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5dd28-299">The Microsoft 365 Apps file list API is used to retrieve the names of the files needed for a particular Microsoft 365 Apps update.</span></span>

<span data-ttu-id="5dd28-300">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="5dd28-300">HTTP Request</span></span>

<span data-ttu-id="5dd28-301">GET https://config.office.com/api/filelist</span><span class="sxs-lookup"><span data-stu-id="5dd28-301">GET https://config.office.com/api/filelist</span></span>

<span data-ttu-id="5dd28-302">N’indiquez pas le corps de la demande pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5dd28-302">Do not supply a request body for this method.</span></span>

<span data-ttu-id="5dd28-303">Aucune autorisation n’est requise pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="5dd28-303">No permissions are required to call this API.</span></span>

<span data-ttu-id="5dd28-304">Paramètres facultatifs de la requête</span><span class="sxs-lookup"><span data-stu-id="5dd28-304">Optional query parameters</span></span>

|<span data-ttu-id="5dd28-305">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5dd28-305">**Name**</span></span>|<span data-ttu-id="5dd28-306">**Description**</span><span class="sxs-lookup"><span data-stu-id="5dd28-306">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5dd28-307">channel</span><span class="sxs-lookup"><span data-stu-id="5dd28-307">channel</span></span> <br/>| <span data-ttu-id="5dd28-308">Spécifie le nom du canal</span><span class="sxs-lookup"><span data-stu-id="5dd28-308">Specifies the channel name</span></span>  <br/> <span data-ttu-id="5dd28-309">Facultatif-valeur par défaut : « semestriel »</span><span class="sxs-lookup"><span data-stu-id="5dd28-309">Optional – default to ‘SemiAnnual’</span></span> <br/> <span data-ttu-id="5dd28-310">Valeurs prises en charge https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span><span class="sxs-lookup"><span data-stu-id="5dd28-310">Supported values https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span></span> |
| <span data-ttu-id="5dd28-311">version</span><span class="sxs-lookup"><span data-stu-id="5dd28-311">version</span></span> <br/>| <span data-ttu-id="5dd28-312">Spécifie la version de mise à jour</span><span class="sxs-lookup"><span data-stu-id="5dd28-312">Specifies the update version</span></span> <br/> <span data-ttu-id="5dd28-313">Optional : valeur par défaut de la dernière version disponible pour le canal spécifié</span><span class="sxs-lookup"><span data-stu-id="5dd28-313">Optional – defaults to the latest version available for the specified channel</span></span> |
| <span data-ttu-id="5dd28-314">arcs</span><span class="sxs-lookup"><span data-stu-id="5dd28-314">arch</span></span> <br/>| <span data-ttu-id="5dd28-315">Spécifie l’architecture client</span><span class="sxs-lookup"><span data-stu-id="5dd28-315">Specifies client architecture</span></span> <br/> <span data-ttu-id="5dd28-316">Optional : par défaut, « x64 »</span><span class="sxs-lookup"><span data-stu-id="5dd28-316">Optional – defaults to ‘x64’</span></span> <br/> <span data-ttu-id="5dd28-317">Valeurs prises en charge : x64, x86</span><span class="sxs-lookup"><span data-stu-id="5dd28-317">Supported values: x64, x86</span></span> |
| <span data-ttu-id="5dd28-318">abattant</span><span class="sxs-lookup"><span data-stu-id="5dd28-318">lid</span></span> <br/>| <span data-ttu-id="5dd28-319">Spécifie les fichiers de langue à inclure</span><span class="sxs-lookup"><span data-stu-id="5dd28-319">Specifies the language files to include</span></span> <br/> <span data-ttu-id="5dd28-320">Facultatif : aucune valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="5dd28-320">Optional – defaults to none</span></span> <br/> <span data-ttu-id="5dd28-321">Pour spécifier plusieurs langues, incluez un paramètre de requête de capot pour chaque langue</span><span class="sxs-lookup"><span data-stu-id="5dd28-321">To specify multiple languages, include an lid query parameter for each language</span></span> <br/> <span data-ttu-id="5dd28-322">Utilisez le format d’identificateur de langue, par exemple.</span><span class="sxs-lookup"><span data-stu-id="5dd28-322">Use the language identifier format, ex.</span></span> <span data-ttu-id="5dd28-323">« en-US », « fr-fr »</span><span class="sxs-lookup"><span data-stu-id="5dd28-323">‘en-us’, ‘fr-fr’</span></span> |
| <span data-ttu-id="5dd28-324">alllanguages</span><span class="sxs-lookup"><span data-stu-id="5dd28-324">alllanguages</span></span> <br/>| <span data-ttu-id="5dd28-325">Spécifie l’inclusion de tous les fichiers de langue</span><span class="sxs-lookup"><span data-stu-id="5dd28-325">Specifies to include all language files</span></span> <br/> <span data-ttu-id="5dd28-326">Facultatif-valeur par défaut : false</span><span class="sxs-lookup"><span data-stu-id="5dd28-326">Optional – defaults to false</span></span> |

<span data-ttu-id="5dd28-327">Réponse HTTP</span><span class="sxs-lookup"><span data-stu-id="5dd28-327">HTTP Response</span></span>

<span data-ttu-id="5dd28-328">Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets file dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="5dd28-328">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="5dd28-329">Pour créer une image, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5dd28-329">To create an image, follow these steps:</span></span>
1.  <span data-ttu-id="5dd28-330">Appelez l’API, en fournissant les paramètres de requête appropriés pour le canal, la version et l’architecture de la mise à jour qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="5dd28-330">Call the API, providing the appropriate query parameters for the channel, version and architecture of the update you are interested in.</span></span>
<span data-ttu-id="5dd28-331">Remarque : les objets file avec l’attribut « LCID » : « 0 » sont des fichiers de langue neutre et doivent être inclus dans l’image.</span><span class="sxs-lookup"><span data-stu-id="5dd28-331">Note: File objects with the attribute "lcid": "0" are language neutral files and must be included in the image.</span></span>
2.  <span data-ttu-id="5dd28-332">Construisez une image locale du CDN en effectuant une itération dans les objets fichier et en copiant les fichiers CDN, lors de la création de la structure de dossiers spécifiée par l’attribut « relativePath » défini pour chaque objet fichier.</span><span class="sxs-lookup"><span data-stu-id="5dd28-332">Construct a local image of the CDN by iterating through the file objects and copying the CDN files, while creating the folder structure as specified by the “relativePath” attribute defined for each of the file objects.</span></span>

<span data-ttu-id="5dd28-333">L’exemple suivant récupère la liste des fichiers du canal actuel et de la version 16.0.4229.1004 pour 64 bits et inclut les fichiers de langue française et anglaise :</span><span class="sxs-lookup"><span data-stu-id="5dd28-333">The following example retrieves the file list for the Current Channel and version 16.0.4229.1004 for 64bit and includes the French and English language files:</span></span>

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="5dd28-334">Vérification de hachage des fichiers. dat</span><span class="sxs-lookup"><span data-stu-id="5dd28-334">Hash verification of .dat files</span></span>

<span data-ttu-id="5dd28-335">Les outils de création d’image peuvent vérifier l’intégrité des fichiers. dat téléchargés en comparant une valeur de hachage calculée avec la valeur de hachage fournie associée à chacun des fichiers. dat.</span><span class="sxs-lookup"><span data-stu-id="5dd28-335">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed hash value with the supplied hash value associated with each of the .dat files.</span></span> <span data-ttu-id="5dd28-336">Voici un exemple d’un objet file qui spécifie les valeurs hashLocation et hashAlgorithm :</span><span class="sxs-lookup"><span data-stu-id="5dd28-336">Following is an example of a file object that specifies hashLocation and hashAlgorithm values:</span></span>
  
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

- <span data-ttu-id="5dd28-337">L’attribut **hashLocation** spécifie l’emplacement de chemin d’accès relatif du fichier. cab qui contient la valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="5dd28-337">The **hashLocation** attribute specifies the relative path location of .cab file that contains the hash value.</span></span> <span data-ttu-id="5dd28-338">Construisez l’emplacement du fichier de hachage en concaténant URL + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="5dd28-338">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="5dd28-339">Dans l’exemple suivant, l’emplacement stream.x64.bg-bg. hash doit être :</span><span class="sxs-lookup"><span data-stu-id="5dd28-339">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="5dd28-340">L’attribut **HashAlgorithm** spécifie l’algorithme de hachage qui a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="5dd28-340">The **hashAlgorithm** attribute specifies what hashing algorithm was used.</span></span> 
    
  <span data-ttu-id="5dd28-341">Pour valider l’intégrité du fichier stream.x64.bg-bg. dat, ouvrez stream.x64.bg-bg. Hash et lisez la valeur de hachage qui est la première ligne de texte dans le fichier de hachage.</span><span class="sxs-lookup"><span data-stu-id="5dd28-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="5dd28-342">Comparez ceci à la valeur de hachage calculée (à l’aide de l’algorithme de hachage spécifié) pour vérifier l’intégrité du fichier. dat téléchargé.</span><span class="sxs-lookup"><span data-stu-id="5dd28-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="5dd28-343">L’exemple suivant montre le code C# permettant de lire le hachage.</span><span class="sxs-lookup"><span data-stu-id="5dd28-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a><span data-ttu-id="5dd28-344">Mises à jour des applications Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5dd28-344">Microsoft 365 Apps Updates</span></span>

<span data-ttu-id="5dd28-345">Toutes les mises à jour des applications Microsoft 365 sont publiées dans le [catalogue Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="5dd28-345">All Microsoft 365 Apps Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="5dd28-346">Les mises à jour des applications Microsoft 365 permettent aux logiciels de gérabilité de traiter les mises à jour des applications Microsoft 365 de la même manière que n’importe quelle autre mise à jour WU, à une exception près : les mises à jour du client ne contiennent pas de charge utile réelle.</span><span class="sxs-lookup"><span data-stu-id="5dd28-346">Microsoft 365 Apps Updates enable manageability software to treat Microsoft 365 Apps Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="5dd28-347">Les mises à jour des applications Microsoft 365 ne doivent pas être installées sur les clients, mais plutôt utilisées pour déclencher les flux de travail avec le logiciel de gérabilité en remplaçant la commande d’installation par le mécanisme d’installation basé sur COM indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5dd28-347">The Microsoft 365 Apps Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span>

<span data-ttu-id="5dd28-348">**La figure suivante illustre un diagramme du flux de travail de mise à jour du client Office 365.**</span><span class="sxs-lookup"><span data-stu-id="5dd28-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="5dd28-349">![Diagramme de flux de travail pour les mises à jour du client O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagramme de flux de travail pour les mises à jour du client O365PP")</span><span class="sxs-lookup"><span data-stu-id="5dd28-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="5dd28-350">Chaque mise à jour des applications Microsoft 365 publiée inclut des métadonnées sur la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5dd28-350">Each Microsoft 365 Apps Update that is published includes metadata about the update.</span></span> <span data-ttu-id="5dd28-351">Ces métadonnées incluent un paramètre nommé MoreInfoUrl qui peut être utilisé pour dériver l’appel de l’API à l’API de liste de fichiers pour cette mise à jour spécifique.</span><span class="sxs-lookup"><span data-stu-id="5dd28-351">This metadata includes a parameter called MoreInfoUrl which can be used to derive the API call to the file list API for that specific update.</span></span>

<span data-ttu-id="5dd28-352">Dans l’exemple suivant, l’API de liste de fichiers est incorporée dans le MoreInfoURL et commence par « ServicePath = »</span><span class="sxs-lookup"><span data-stu-id="5dd28-352">In the following example, the file list API is embedded in the MoreInfoURL and starts with “ServicePath=”</span></span>

<span data-ttu-id="5dd28-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath =https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span><span class="sxs-lookup"><span data-stu-id="5dd28-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span></span>
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="5dd28-354">Métadonnées supplémentaires pour l’automatisation du transfert de contenu</span><span class="sxs-lookup"><span data-stu-id="5dd28-354">Additional metadata for automating content staging</span></span>

<span data-ttu-id="5dd28-355">**API d’historique des versions**</span><span class="sxs-lookup"><span data-stu-id="5dd28-355">**Release History API**</span></span>
  
<span data-ttu-id="5dd28-356">L’API d’historique de publication des applications Microsoft 365 est utilisée pour récupérer les détails de chacune des mises à jour publiées sur le CDN, ainsi que les noms de canal et d’autres attributs de canal.</span><span class="sxs-lookup"><span data-stu-id="5dd28-356">The Microsoft 365 Apps release history API is used to retrieve details for each of the updates published to the CDN along with the channel names and other channel attributes.</span></span>

<span data-ttu-id="5dd28-357">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="5dd28-357">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/channels 
```

<span data-ttu-id="5dd28-358">N’indiquez pas le corps de la demande pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5dd28-358">Do not supply a request body for this method.</span></span>

<span data-ttu-id="5dd28-359">Aucune autorisation n’est requise pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="5dd28-359">No permissions are required to call this API.</span></span>

<span data-ttu-id="5dd28-360">Réponse HTTP</span><span class="sxs-lookup"><span data-stu-id="5dd28-360">HTTP Response</span></span>

<span data-ttu-id="5dd28-361">Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets file dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="5dd28-361">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="5dd28-362">**API UGS**</span><span class="sxs-lookup"><span data-stu-id="5dd28-362">**SKUs API**</span></span>
  
<span data-ttu-id="5dd28-363">L’API SKU renvoie des informations utiles pour déterminer les produits disponibles pour le déploiement et la maintenance à partir du CDN Office, ainsi que diverses options pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="5dd28-363">The SKUs API returns information that is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span>

<span data-ttu-id="5dd28-364">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="5dd28-364">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/skus 
```

<span data-ttu-id="5dd28-365">N’indiquez pas le corps de la demande pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5dd28-365">Do not supply a request body for this method.</span></span>

<span data-ttu-id="5dd28-366">Aucune autorisation n’est requise pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="5dd28-366">No permissions are required to call this API.</span></span>

<span data-ttu-id="5dd28-367">Réponse HTTP</span><span class="sxs-lookup"><span data-stu-id="5dd28-367">HTTP Response</span></span>

<span data-ttu-id="5dd28-368">Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets file dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="5dd28-368">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>
