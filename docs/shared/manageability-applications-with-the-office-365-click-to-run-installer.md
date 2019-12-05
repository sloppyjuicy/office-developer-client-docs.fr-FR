---
title: Intégration des applications de gestion avec le programme d’installation Office 365 « démarrer en un clic »
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Découvrez comment intégrer le programme d’installation Office 365 « démarrer en un clic » à une solution de gestion de logiciels.
ms.openlocfilehash: 62bfef0063c414fcecd0948e49dfa098b5c82bbb
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819272"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a><span data-ttu-id="71deb-103">Intégration des applications de gestion avec le programme d’installation Office 365 « démarrer en un clic »</span><span class="sxs-lookup"><span data-stu-id="71deb-103">Integrating manageability applications with Office 365 click-to-run installer</span></span>

<span data-ttu-id="71deb-104">Découvrez comment intégrer le programme d’installation Office 365 « démarrer en un clic » à une solution de gestion de logiciels.</span><span class="sxs-lookup"><span data-stu-id="71deb-104">Learn how to integrate the Office 365 Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="71deb-105">Le programme d’installation Office 365 « démarrer en un clic » fournit une interface COM qui permet aux professionnels de l’informatique et au contrôle par programme des solutions de gestion des logiciels de gérer les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-105">The Office 365 Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="71deb-106">Cette interface fournit des fonctionnalités de gestion supplémentaires au-delà de ce qui est fourni par l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="71deb-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="71deb-107">Cet article s’applique à Office 2016 et versions ultérieures, Office 365.</span><span class="sxs-lookup"><span data-stu-id="71deb-107">This article applies to Office 2016 and later, Office 365.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="71deb-108">Intégration à « démarrer en un clic »</span><span class="sxs-lookup"><span data-stu-id="71deb-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="71deb-109">Pour utiliser cette interface, une application de gérabilité appelle l’interface COM et appelle des API exposées qui communiquent directement avec le service d’installation « démarrer en un clic ».</span><span class="sxs-lookup"><span data-stu-id="71deb-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="71deb-110">Le programme d’installation Office « démarrer en un clic » peut être exécuté à partir de la ligne de commande avec des paramètres qui peuvent contrôler le comportement, comme indiqué dans l' [outil déploiement d’Office pour démarrer en un clic](https://www.microsoft.com/download/details.aspx?id=49117).</span><span class="sxs-lookup"><span data-stu-id="71deb-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span> 
  
<span data-ttu-id="71deb-111">**Voici un diagramme conceptuel de l’interface COM**</span><span class="sxs-lookup"><span data-stu-id="71deb-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="71deb-112">![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM sur le programme d’installation Office « démarrer en un clic »")</span><span class="sxs-lookup"><span data-stu-id="71deb-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="71deb-113">Le programme d’installation Office « démarrer en un clic » d’Office 365 implémente une interface COM, **IUpdateNotify** inscrite au CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="71deb-113">The Office 365 Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="71deb-114">Cette interface peut être appelée comme suit :</span><span class="sxs-lookup"><span data-stu-id="71deb-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="71deb-115">L’appel ne réussira que si l’appelant s’exécute sous des privilèges élevés, car le programme d’installation démarrer en un clic doit être exécuté avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="71deb-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="71deb-116">L’interface com **IUpdateNotify** expose trois fonctions asynchrones chargées de la validation des commandes et des paramètres et de l’exécution de la planification avec le service d’installation « démarrer en un clic ».</span><span class="sxs-lookup"><span data-stu-id="71deb-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="71deb-117">Une méthode, **Status**, peut être utilisée pour obtenir des informations sur l’état de la dernière commande exécutée ou l’état de la commande en cours d’exécution (c.-à-d. réussite, échec, codes d’erreur détaillés).</span><span class="sxs-lookup"><span data-stu-id="71deb-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="71deb-118">Il existe quatre États selon lesquels le service d’installation « démarrer en un clic » peut se trouver pendant son cycle de vie, pendant laquelle les méthodes **IUpdateNotify** peuvent être appelées ; Redémarrage, inactivité, téléchargement et application.</span><span class="sxs-lookup"><span data-stu-id="71deb-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="71deb-119">**Le schéma de machine à États de l’interface COM est le suivant :**</span><span class="sxs-lookup"><span data-stu-id="71deb-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="71deb-120">![Diagramme d’état pour l’interface COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Diagramme d’État pour l’interface COM")</span><span class="sxs-lookup"><span data-stu-id="71deb-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="71deb-121">**Redémarrage**: lors du démarrage de l’ordinateur, le service d’installation « démarrer en un clic » n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="71deb-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="71deb-122">Un appel réussi à la méthode Status après un redémarrage renverra eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="71deb-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="71deb-123">**Inactif :** Lorsque le programme d’installation « démarrer en un clic » est à l’état inactif, vous pouvez appeler les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="71deb-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="71deb-124">**Appliquer**: installer le contenu précédemment téléchargé.</span><span class="sxs-lookup"><span data-stu-id="71deb-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="71deb-125">**Cancel**: renvoie `0x800000e`, « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="71deb-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="71deb-126">**Téléchargement**: télécharge le nouveau contenu sur le client pour une installation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="71deb-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="71deb-127">**État**: renvoie le résultat de la dernière action terminée ou un message d’erreur si l’action s’est terminée en raison d’un échec.</span><span class="sxs-lookup"><span data-stu-id="71deb-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="71deb-128">S’il n’existe aucune action précédente, **Status** renvoie `eUPDATE_UNKNOWN`.</span><span class="sxs-lookup"><span data-stu-id="71deb-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="71deb-129">**Téléchargement :** Lorsque le programme d’installation démarrer en un clic est à l’état de téléchargement, vous pouvez appeler les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="71deb-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="71deb-130">**Apply**: retourne un **HRESULT** avec la valeur `0x800000e`« une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="71deb-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="71deb-131">**Cancel**: arrête le téléchargement et supprime le contenu partiellement téléchargé.</span><span class="sxs-lookup"><span data-stu-id="71deb-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="71deb-132">**Téléchargement**: retourne un **HRESULT** avec la valeur `0x800000e`« une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="71deb-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="71deb-133">**Status**: renvoie **DOWNLOAD_WIP** pour indiquer que le téléchargement est en cours.</span><span class="sxs-lookup"><span data-stu-id="71deb-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="71deb-134">**Application :** Lorsque le programme d’installation « démarrer en un clic » se trouve dans le processus d’installation du contenu précédemment téléchargé :</span><span class="sxs-lookup"><span data-stu-id="71deb-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="71deb-135">**Apply**: retourne un **HRESULT** avec la valeur `0x800000e`« une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="71deb-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="71deb-136">**Cancel**: renvoie `0x800000e`, l’action Apply ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="71deb-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="71deb-137">**Téléchargement**: retourne un **HRESULT** avec la valeur `0x800000e`« une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="71deb-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="71deb-138">**État**: renvoie **APPLY_WIP** pour indiquer que l’opération d’application est en cours.</span><span class="sxs-lookup"><span data-stu-id="71deb-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="71deb-139">Étant donné que OfficeC2RCOM est un service COM+ et qu’il est chargé dynamiquement, vous devez appeler **CoCreateInstance** chaque fois que vous appelez une méthode sur cette classe afin de vous assurer que vous obtenez le résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="71deb-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="71deb-140">Le service COM+ gère la création d’une nouvelle instance si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="71deb-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="71deb-141">Lorsqu’une des méthodes est appelée pour la première fois, COM+ charge l’objet **IUpdateNotify** et l’exécute dans l’une des instances de Dllhost. exe.</span><span class="sxs-lookup"><span data-stu-id="71deb-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="71deb-142">Le nouvel objet reste actif pendant environ 3 minutes d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="71deb-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="71deb-143">Si un appel est effectué dans les trois minutes suivant le dernier appel, l’objet **IUpdateNotify** reste chargé et une nouvelle instance n’est pas créée.</span><span class="sxs-lookup"><span data-stu-id="71deb-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="71deb-144">Si aucun appel n’est effectué dans les trois minutes, l’objet IUpdateNotify est déchargé et un nouvel objet **IUpdateNotify** est créé lors de l’appel suivant.</span><span class="sxs-lookup"><span data-stu-id="71deb-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="71deb-145">Guide de référence de l’API COM « démarrer en un clic »</span><span class="sxs-lookup"><span data-stu-id="71deb-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="71deb-146">Dans la documentation de référence de l’API suivante :</span><span class="sxs-lookup"><span data-stu-id="71deb-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="71deb-147">Les paramètres se trouvent dans un format de paire clé/valeur séparé par un espace.</span><span class="sxs-lookup"><span data-stu-id="71deb-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="71deb-148">Les paramètres ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="71deb-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="71deb-149">Il existe une [liste de paramètres](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) avec la documentation disponible.</span><span class="sxs-lookup"><span data-stu-id="71deb-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="71deb-150">Le résumé de l’interface IUpdateNotify2 est désormais inclus.</span><span class="sxs-lookup"><span data-stu-id="71deb-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="71deb-151">Appliquer</span><span class="sxs-lookup"><span data-stu-id="71deb-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="71deb-152">Parameters</span><span class="sxs-lookup"><span data-stu-id="71deb-152">Parameters</span></span>

-  <span data-ttu-id="71deb-153">_DisplayLevel_: **true** pour afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false** pour masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="71deb-154">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="71deb-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="71deb-155">_forceappshutdown_: **true** pour obliger les applications Office à s’arrêter immédiatement lorsque l’action d' **application** est déclenchée ; **false** pour faire échouer si des applications Office sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="71deb-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="71deb-156">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="71deb-156">The default is **false**.</span></span> <span data-ttu-id="71deb-157">Pour plus d’informations, voir [Remarques](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="71deb-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="71deb-158">Si une application Office est en cours d’exécution lorsque l’action d' **application** est déclenchée **, l’action d’application échoue** généralement.</span><span class="sxs-lookup"><span data-stu-id="71deb-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="71deb-159">En `forceappshutdown=true` passant à la méthode **apply** , le service **OfficeClickToRun** arrête immédiatement les applications et applique la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="71deb-160">Dans ce cas, l’utilisateur peut subir une perte de données.</span><span class="sxs-lookup"><span data-stu-id="71deb-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="71deb-161">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="71deb-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71deb-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="71deb-162">**S_OK**</span></span> <br/> |<span data-ttu-id="71deb-163">L’action a été correctement envoyée au service « démarrer en un clic » pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="71deb-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="71deb-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="71deb-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="71deb-165">L’appelant n’est pas en cours d’exécution avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="71deb-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="71deb-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="71deb-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="71deb-167">Les paramètres non valides ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="71deb-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="71deb-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="71deb-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="71deb-169">L’action n’est pas autorisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="71deb-169">Action is not allowed at this time.</span></span> <span data-ttu-id="71deb-170">Pour plus d’informations, voir [Remarques](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="71deb-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="71deb-171">Remarques</span><span class="sxs-lookup"><span data-stu-id="71deb-171">Remarks</span></span>

- <span data-ttu-id="71deb-172">Si une application Office est en cours d’exécution lorsque l’action d' **application** est déclenchée **, l’action d’application échoue** .</span><span class="sxs-lookup"><span data-stu-id="71deb-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="71deb-173">En `forceappshutdown=true` passant à la méthode **apply** , le service **OfficeClickToRun** arrête immédiatement toutes les applications Office en cours d’exécution et applique la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="71deb-174">L’utilisateur peut se servir des données, car il n’est pas invité à enregistrer les modifications apportées aux documents ouverts..</span><span class="sxs-lookup"><span data-stu-id="71deb-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="71deb-175">Cette action ne peut être déclenchée que lorsque le statut COM est l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="71deb-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="71deb-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="71deb-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="71deb-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="71deb-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="71deb-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="71deb-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="71deb-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="71deb-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="71deb-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="71deb-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="71deb-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="71deb-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="71deb-182">Si vous appelez la méthode **apply** sans télécharger le contenu précédemment, la méthode **apply** signalera la **réussite** car elle n’a pas pu s’appliquer et a terminé le processus d' **application** .</span><span class="sxs-lookup"><span data-stu-id="71deb-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="71deb-183">Annuler</span><span class="sxs-lookup"><span data-stu-id="71deb-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="71deb-184">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="71deb-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71deb-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="71deb-185">S_OK</span></span>  <br/> |<span data-ttu-id="71deb-186">L’action a été correctement envoyée au service « démarrer en un clic » pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="71deb-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="71deb-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="71deb-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="71deb-188">L’action n’est pas autorisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="71deb-188">Action is not allowed at this time.</span></span> <span data-ttu-id="71deb-189">Pour plus d’informations, consultez la section [Remarques](#bk_CancelRemarks) .</span><span class="sxs-lookup"><span data-stu-id="71deb-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="71deb-190">Remarques</span><span class="sxs-lookup"><span data-stu-id="71deb-190">Remarks</span></span>

- <span data-ttu-id="71deb-191">Cette méthode ne peut être déclenchée que lorsque l’ID d’État COM **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="71deb-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="71deb-192">Elle tentera d’annuler l’action de téléchargement en cours.</span><span class="sxs-lookup"><span data-stu-id="71deb-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="71deb-193">L’état de COM passe à **eDOWNLOAD_CANCELLING** et change finalement en **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="71deb-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="71deb-194">L’État COM renvoie **E_ILLEGAL_METHOD_CALL** s’il est déclenché à tout autre moment.</span><span class="sxs-lookup"><span data-stu-id="71deb-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="71deb-195">Téléchargement</span><span class="sxs-lookup"><span data-stu-id="71deb-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="71deb-196">Parameters</span><span class="sxs-lookup"><span data-stu-id="71deb-196">Parameters</span></span>

-  <span data-ttu-id="71deb-197">_DisplayLevel_: **true** pour afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false** pour masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="71deb-198">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="71deb-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="71deb-199">_updatebaseurl_: URL vers l’autre source de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="71deb-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="71deb-200">_updatetoversion_: version à mettre à jour Office vers.</span><span class="sxs-lookup"><span data-stu-id="71deb-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="71deb-201">Définissez ce paramètre si vous souhaitez effectuer une mise à jour vers une version antérieure à la version actuellement installée.</span><span class="sxs-lookup"><span data-stu-id="71deb-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="71deb-202">_downloadsource_: CLSID de l’implémentation **IBackgroundCopyManager** personnalisée (gestionnaire bits).</span><span class="sxs-lookup"><span data-stu-id="71deb-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="71deb-203">_contentid_: identifie le contenu à télécharger à partir du serveur de contenu via le gestionnaire des bits personnalisé.</span><span class="sxs-lookup"><span data-stu-id="71deb-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="71deb-204">Cette valeur est transmise à l’interprétation via l’interface BITS.</span><span class="sxs-lookup"><span data-stu-id="71deb-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="71deb-205">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="71deb-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71deb-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="71deb-206">**S_OK**</span></span> <br/> |<span data-ttu-id="71deb-207">L’action a été correctement envoyée au service « démarrer en un clic » pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="71deb-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="71deb-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="71deb-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="71deb-209">L’appelant n’est pas en cours d’exécution avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="71deb-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="71deb-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="71deb-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="71deb-211">Les paramètres non valides ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="71deb-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="71deb-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="71deb-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="71deb-213">L’action n’est pas autorisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="71deb-213">Action is not allowed at this time.</span></span> <span data-ttu-id="71deb-214">Pour plus d’informations, voir [Remarques](#bk_DownloadRemark) .</span><span class="sxs-lookup"><span data-stu-id="71deb-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="71deb-215">Remarques</span><span class="sxs-lookup"><span data-stu-id="71deb-215">Remarks</span></span>

- <span data-ttu-id="71deb-216">Vous devez spécifier _downloadsource_ et _contentid_ en tant que paire.</span><span class="sxs-lookup"><span data-stu-id="71deb-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="71deb-217">Si ce n’est pas le cas, la méthode de **Téléchargement** renvoie une erreur **E_INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="71deb-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="71deb-218">Si _downloadsource_, _contentid_et _updatebaseurl_ sont fournis, _updatebaseurl_ sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="71deb-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="71deb-219">Cette action ne peut être déclenchée que lorsque le statut COM est l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="71deb-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="71deb-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="71deb-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="71deb-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="71deb-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="71deb-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="71deb-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="71deb-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="71deb-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="71deb-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="71deb-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="71deb-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="71deb-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="71deb-226">Si vous appelez la méthode **apply** sans le contenu précédemment téléchargé, la méthode **apply** signalera la **réussite** car elle n’a pas pu s’appliquer et a terminé le processus d' **application** .</span><span class="sxs-lookup"><span data-stu-id="71deb-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="71deb-227">Exemples</span><span class="sxs-lookup"><span data-stu-id="71deb-227">Examples</span></span>

- <span data-ttu-id="71deb-228">Pour télécharger le contenu à partir du gestionnaire des fichiers BITS personnalisé : appelez la fonction **Download ()** en transmettant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="71deb-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="71deb-229">Pour télécharger le contenu à partir du CDN Microsoft : appelez la fonction **Download ()** sans spécifier les paramètres _downloadsource_, _contentid_ou _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="71deb-229">To download the content from the Microsoft CDN: Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="71deb-230">Pour télécharger le contenu à partir d’un emplacement personnalisé : appelez la fonction **Download ()** en transmettant le paramètre suivant :</span><span class="sxs-lookup"><span data-stu-id="71deb-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="71deb-231">Statut</span><span class="sxs-lookup"><span data-stu-id="71deb-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="71deb-232">Parameters</span><span class="sxs-lookup"><span data-stu-id="71deb-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="71deb-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="71deb-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="71deb-234">Pointeur vers une structure UPDATE_STATUS_REPORT.</span><span class="sxs-lookup"><span data-stu-id="71deb-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="71deb-235">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="71deb-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71deb-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="71deb-236">**S_OK**</span></span> <br/> |<span data-ttu-id="71deb-237">La méthode **Status** renvoie toujours ce résultat.</span><span class="sxs-lookup"><span data-stu-id="71deb-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="71deb-238">Inspectez `UPDATE_STATUS_RESULT` la structure pour connaître l’état de l’action actuelle.</span><span class="sxs-lookup"><span data-stu-id="71deb-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="71deb-239">Remarques</span><span class="sxs-lookup"><span data-stu-id="71deb-239">Remarks</span></span>

- <span data-ttu-id="71deb-240">Champ d’état de la `UPDATE_STATUS_REPORT` contient l’état de l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="71deb-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="71deb-241">L’une des valeurs d’État suivantes est renvoyée :</span><span class="sxs-lookup"><span data-stu-id="71deb-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="71deb-242">Si la dernière commande a généré une erreur, le champ d’erreur de `UPDATE_STATUS_REPORT` contient des informations détaillées sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="71deb-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="71deb-243">Deux types de codes d’erreur sont renvoyés à partir de la méthode **Status** .</span><span class="sxs-lookup"><span data-stu-id="71deb-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="71deb-244">Si l’erreur est inférieure `UPDATE_ERROR_CODE::eUNKNOWN`à, l’erreur est l’un des codes d’erreur prédéfinis suivants :</span><span class="sxs-lookup"><span data-stu-id="71deb-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="71deb-245">Si le code d’erreur renvoyé est plus `UPDATE_ERROR_CODE::eUNKNOWN` grand que le **HRESULT** d’un appel de fonction ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="71deb-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="71deb-246">Pour extraire la soustraction `UPDATE_ERROR_CODE::eUNKNOWN` HRESULT de la valeur renvoyée dans le champ Error `UPDATE_STATUS_REPORT`du.</span><span class="sxs-lookup"><span data-stu-id="71deb-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="71deb-247">La liste complète des valeurs d’État et d’erreur peut être affichée en inspectant la bibliothèque de types **IUpdateNotify** incorporée dans OfficeC2RCom. dll.</span><span class="sxs-lookup"><span data-stu-id="71deb-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="71deb-248">Le champ contentid est utilisé pour les appels à l' **État** après le **Téléchargement** et renvoie le contentid qui a été transmis à l’appel de **Téléchargement** .</span><span class="sxs-lookup"><span data-stu-id="71deb-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="71deb-249">Il est recommandé d’initialiser ce champ sur **null** avant d’appeler la méthode **Status** , puis de vérifier la valeur après que **Status** a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="71deb-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="71deb-250">Si la valeur est toujours **null**, cela signifie qu’il n’existe aucun contentid à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="71deb-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="71deb-251">Si la valeur n’est pas **null**, vous devez la libérer avec un appel à **SysFreeString ()**.</span><span class="sxs-lookup"><span data-stu-id="71deb-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="71deb-252">Voici un extrait de code expliquant comment appeler l' **État** après le **Téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="71deb-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="71deb-253">Résumé de l’interface IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="71deb-253">Summary of IUpdateNotify2 interface</span></span>

> [!NOTE]
> <span data-ttu-id="71deb-254">Ce résumé fournit des informations complémentaires sur [l’intégration des applications de gestion avec le programme d’installation Office 365 « démarrer en un clic »](https://docs.microsoft.com/office/client-developer/shared/manageability-applications-with-the-office-365-click-to-run-installer).</span><span class="sxs-lookup"><span data-stu-id="71deb-254">This summary is provided as a compliment info to [Integrating manageability applications with the Office 365 click-to-run installer](https://docs.microsoft.com/office/client-developer/shared/manageability-applications-with-the-office-365-click-to-run-installer).</span></span> <span data-ttu-id="71deb-255">Une fois le document public mis à jour, ce document peut être considéré comme obsolète.</span><span class="sxs-lookup"><span data-stu-id="71deb-255">Once the public doc is updated, this doc can be considered as obsolete.</span></span> 
  
<span data-ttu-id="71deb-256">À partir de C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (la première Build publiquement disponible doit être la version de la branche de juin 8326. \*), nous avons ajouté une nouvelle interface **IUpdateNotify2** .</span><span class="sxs-lookup"><span data-stu-id="71deb-256">From C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (First publicly available build should be June fork build -- 8326.\*) we have added a new **IUpdateNotify2** interface.</span></span> <span data-ttu-id="71deb-257">Voici quelques informations de base sur cette interface :</span><span class="sxs-lookup"><span data-stu-id="71deb-257">Here is some basic info about this interface:</span></span> 
  
- <span data-ttu-id="71deb-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="71deb-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="71deb-259">Cette interface hébergeait également l’interface IUpdateNotify d’origine pour assurer la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="71deb-259">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="71deb-260">Cela signifie que si vous utilisez cette interface, vous avez accès à toutes les méthodes fournies dans l’interface **UpdateNotifyObject** .</span><span class="sxs-lookup"><span data-stu-id="71deb-260">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="71deb-261">Nouvelles méthodes ajoutées à IUpdateNotify2 :</span><span class="sxs-lookup"><span data-stu-id="71deb-261">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="71deb-262">**HRESULT** GetBlockingApps ([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="71deb-262">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="71deb-263">Obtenir la liste des applications de blocage des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-263">Get updates blocking apps list.</span></span> <span data-ttu-id="71deb-264">Cet appel renverra les applications Office en cours d’exécution, ce qui bloquera le processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-264">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="71deb-265">**HRESULT** GetOfficeDeploymentData ([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="71deb-265">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="71deb-266">Obtenir les données de déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="71deb-266">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="71deb-267">Si vous souhaitez utiliser les nouvelles méthodes, vous devez vous assurer que :</span><span class="sxs-lookup"><span data-stu-id="71deb-267">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="71deb-268">Votre version d’C2R est plus récente que la build\>ci-dessus (version de la partie juin).</span><span class="sxs-lookup"><span data-stu-id="71deb-268">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="71deb-269">Utilisez UpdateNotifyObject2 au lieu de **UpdateNotifyObject** pour appeler **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="71deb-269">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="71deb-270">Si vous n’utilisez aucune des nouvelles méthodes, vous n’avez pas besoin de modifier quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="71deb-270">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="71deb-271">Toutes les méthodes existantes fonctionneront exactement de la même manière qu’avant.</span><span class="sxs-lookup"><span data-stu-id="71deb-271">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="71deb-272">Implémentation de l’interface BITS</span><span class="sxs-lookup"><span data-stu-id="71deb-272">Implementing the BITS interface</span></span>

<span data-ttu-id="71deb-273">Le [service de transfert intelligent en arrière-plan](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (bits) est un service fourni par Microsoft pour transférer des fichiers entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="71deb-273">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="71deb-274">BITS est l’un des canaux que le programme d’installation d’Office « démarrer en un clic » peut utiliser pour télécharger du contenu.</span><span class="sxs-lookup"><span data-stu-id="71deb-274">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="71deb-275">Par défaut, le programme d’installation Office « démarrer en un clic » utilise l’implémentation intégrée de Windows pour télécharger le contenu à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="71deb-275">By default, the Office Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="71deb-276">En fournissant une implémentation BITS personnalisée à la méthode de **téléchargement ()** de l’interface **IUpdateNotify** , votre logiciel de gestion peut contrôler l’emplacement et la façon dont le client télécharge le contenu.</span><span class="sxs-lookup"><span data-stu-id="71deb-276">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="71deb-277">Une interface BITS personnalisée est utile lorsque vous fournissez un canal de distribution de contenu personnalisé autre que les canaux intégrés « démarrer en un clic », tels que le CDN Office, les serveurs IIS ou les partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="71deb-277">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the Office CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="71deb-278">La configuration minimale requise pour une interface BITS personnalisée pour fonctionner avec le service Office C2R est la suivante :</span><span class="sxs-lookup"><span data-stu-id="71deb-278">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="71deb-279">Pour **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="71deb-279">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="71deb-280">Pour **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="71deb-280">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="71deb-281">Pour **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="71deb-281">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="71deb-282">Pour les `Addfile` fonctions `AddFileWithRanges` et, l’URL distante est au format suivant :</span><span class="sxs-lookup"><span data-stu-id="71deb-282">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="71deb-283">cmbits est codé en dur et représente des BITS personnalisés.</span><span class="sxs-lookup"><span data-stu-id="71deb-283">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="71deb-284">__ \*\*\*\* _\> contentid est le paramètre contentid de la méthode \<_ Download ().</span><span class="sxs-lookup"><span data-stu-id="71deb-284">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="71deb-285">_chemin d’accès relatif au\> fichier cible fournit l’emplacement et le nom de fichier du fichier à télécharger. \<_</span><span class="sxs-lookup"><span data-stu-id="71deb-285">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="71deb-286">Par exemple, si vous avez fourni un _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` à la **méthode Download ()** et que Office C2R souhaite télécharger le fichier CAB de la version, par `v32.cab` exemple fichier, il appellera **AddFile ()** avec les éléments `RemoteUrl`suivants :</span><span class="sxs-lookup"><span data-stu-id="71deb-286">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="71deb-287">Pour **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="71deb-287">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="71deb-288">Pour **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="71deb-288">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://docs.microsoft.com/DeployOffice/overview-of-update-channels-for-office-365-proplus) using the [Office 2016 Deployment Tool](https://www.microsoft.com/download/details.aspx?id=49117) or [System Center Configuration Manager](https://docs.microsoft.com/deployoffice/manage-office-365-proplus-updates-with-configuration-manager).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
- O365Client_32bit.xml
    
- O365Client_64bit.xml
    
Within the XML for each of the file lists is an  `UpdateFiles` node which contains a version attribute.  `UpdateFiles version="1.4"`.
  
This version is incremented if changes are made to the file lists.
  
There are two parameters that need to be combined with the XML to make a custom image: 
  
- Replace  _%version%_ with the build version of Office. This can be derived from the Client Update metadata  `MoreInfoURL` field, see below. 
    
- Define  _baseURL_ by using the URL value associated with the branch the image is being created for. This can be derived from the Client Update metadata, see below. 
    
The steps for creating an image are:
  
1. Open the XML file list.
    
2. Replace occurrences of  _%version%_ with the applicable Office build version. The build version can be acquired from releasehistory.xml as described later in this article. 
    
3. Read the URL attribute for the target branch.
    
4. Remove language nodes for any languages not required in the custom image.
    
   > [!NOTE]
   > Nodes with language='0' are language neutral and must be included in the image. 
  
5. Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed. 
    
   - If the  _rename_ attribute is provided, then rename the copied file to the value provided in the  _rename_ attribute. This used to create the top-level default v64.cab and v32.cab files. These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified. 
    
   - Use URL + relativePath + filename to construct the CDN location.
    
The following examples use the Monthly channel (as defined by the  `baseURL` node) and build version 16.0.4229.1004 from releasehistory.xml. 
  
```cpp
baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
- The  _hashAlgo_ attribute specifies what hashing algorithm was used. In this case the Sha256 algorithm was used. 
    
To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the hash value from the first line of text in the hash file. Compare this to the has value that you computed using the specified hashing algorithm to verify that the values match. Use the following C# code to read the hash.
  
```cs
string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
string readHash = readHashes.First();

```

### Office 365 Client Updates

Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload. The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.
  
**Office 365 Client Update workflow**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")
  
Each Office 365 Client Update that is published includes metadata about the update. This metadata includes a parameter called  _MoreInfoUrl_ which can be used to derive the following information: 
  
-  _Ver_: Identifies the Office version associated with this update. For example 16.0.4229.1004.
    
-  _Branch_: Identifies the Update Channel for this update. Values include InsiderFast, Insiders, Monthly, Targeted, Broad. Additional values may be added in the future.
    
-  _Arch_: Identifies the processor architecture associated with this update.
    
-  _xmlVer_: Identifies the version of the XML file lists to use to construct the base image for this update.
    
-  _xmlPath_: Path to the OFL.CAB file that contains the XML file lists.
    
-  _xmlFile_: The name of the file list that should be used for this update. The value will be  `O365Client_32bit` or  `O365Client_64bit` and will match the value in  _Arch_.
    
The following is an example of the  _MoreInfoURL_ parameter which refers to the Office 365 Client Update for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel. 
  
```http
https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a><span data-ttu-id="71deb-289">Automatisation du transfert de contenu</span><span class="sxs-lookup"><span data-stu-id="71deb-289">Automating content staging</span></span>

<span data-ttu-id="71deb-290">Les administrateurs informatiques peuvent choisir d’activer la réception automatique des mises à jour lorsqu’elles sont disponibles directement à partir du réseau de distribution de contenu Microsoft (CDN) ou choisir de contrôler le déploiement des mises à jour disponibles à partir de la mise à jour. canaux à l’aide de l’outil déploiement d’Office ou de System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="71deb-290">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or System Center Configuration Manager.</span></span>
  
<span data-ttu-id="71deb-291">Le service prend en charge la possibilité pour les outils de gestion de reconnaître et d’automatiser le téléchargement du contenu lorsque des mises à jour sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="71deb-291">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="71deb-292">**L’image suivante est une vue d’ensemble du téléchargement d’une image personnalisée**</span><span class="sxs-lookup"><span data-stu-id="71deb-292">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="71deb-293">![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme de l’utilisation de l’interface COM sur le programme d’installation Office « démarrer en un clic »")</span><span class="sxs-lookup"><span data-stu-id="71deb-293">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="71deb-294">Vue d’ensemble du téléchargement d’une image personnalisée</span><span class="sxs-lookup"><span data-stu-id="71deb-294">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="71deb-295">Dans le diagramme précédent, vous voyez qu’une nouvelle image Office 365 ProPlus est disponible sur le réseau de distribution de contenu (CDN) Office.</span><span class="sxs-lookup"><span data-stu-id="71deb-295">In the previous diagram, you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN).</span></span> <span data-ttu-id="71deb-296">En plus de l’image Office 365 ProPlus, une liste de fichiers au format XML est également disponible, qui contient les informations nécessaires pour permettre aux logiciels de gestion de créer directement des images personnalisées, qui remplacent la nécessité d’utiliser l’outil déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="71deb-296">Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>
  
<span data-ttu-id="71deb-297">Une entreprise configure son WSUS pour synchroniser les mises à jour du client Office 365.</span><span class="sxs-lookup"><span data-stu-id="71deb-297">An enterprise configures their WSUS to sync the Office 365 Client Updates.</span></span> <span data-ttu-id="71deb-298">Ces mises à jour ne contiennent pas la charge utile de l’image réelle, mais elles permettent au logiciel de gérabilité de reconnaître quand un nouveau contenu est disponible.</span><span class="sxs-lookup"><span data-stu-id="71deb-298">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="71deb-299">Le logiciel de gestion peut ensuite lire les métadonnées de mise à jour du client pour comprendre la version d’Office à laquelle s’applique la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-299">The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.</span></span>
  
<span data-ttu-id="71deb-300">Si la mise à jour est applicable, le logiciel de gestion peut utiliser le contenu CDN et la liste des fichiers pour créer l’image personnalisée et la stocker sur l’emplacement de partage de fichiers qu’elle est configurée à utiliser.</span><span class="sxs-lookup"><span data-stu-id="71deb-300">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="format-of-the-xml-file-list"></a><span data-ttu-id="71deb-301">Format de la liste de fichiers XML</span><span class="sxs-lookup"><span data-stu-id="71deb-301">Format of the XML file list</span></span>

<span data-ttu-id="71deb-302">Deux listes de fichiers sont disponibles dans un fichier cab sur le CDN.</span><span class="sxs-lookup"><span data-stu-id="71deb-302">There are two file lists available in a cab file on the CDN.</span></span> <span data-ttu-id="71deb-303">L’une répertorie les fichiers pour la version 32 bits d’Office et l’autre pour la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="71deb-303">One lists the files for the 32-bit version of Office and one for the 64-bit version of Office.</span></span> <span data-ttu-id="71deb-304">URL de l’emplacement de la liste de fichiers Office (OFL. CAB) est [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span><span class="sxs-lookup"><span data-stu-id="71deb-304">The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span></span> <span data-ttu-id="71deb-305">Les deux listes de fichiers sont appelées :</span><span class="sxs-lookup"><span data-stu-id="71deb-305">The two file lists are called:</span></span>
  
- <span data-ttu-id="71deb-306">O365Client_32bit. Xml</span><span class="sxs-lookup"><span data-stu-id="71deb-306">O365Client_32bit.xml</span></span>
    
- <span data-ttu-id="71deb-307">O365Client_64bit. Xml</span><span class="sxs-lookup"><span data-stu-id="71deb-307">O365Client_64bit.xml</span></span>
    
<span data-ttu-id="71deb-308">Dans le code XML de chacune des listes de fichiers se <UpdateFiles> trouve un nœud qui contient un attribut de version.</span><span class="sxs-lookup"><span data-stu-id="71deb-308">Within the XML for each of the file lists is an <UpdateFiles> node which contains a version attribute.</span></span>  <span data-ttu-id="71deb-309">`<UpdateFiles version="1.4">`.</span><span class="sxs-lookup"><span data-stu-id="71deb-309"></span></span> <span data-ttu-id="71deb-310">Cette version est incrémentée si des modifications sont apportées aux listes de fichiers.</span><span class="sxs-lookup"><span data-stu-id="71deb-310">This version is incremented if changes are made to the file lists.</span></span>
  
<span data-ttu-id="71deb-311">Deux paramètres doivent être combinés avec le code XML pour créer une image personnalisée :</span><span class="sxs-lookup"><span data-stu-id="71deb-311">There are two parameters that need to be combined with the XML to make a custom image:</span></span> 
  
- <span data-ttu-id="71deb-312">Remplacez *% version%* par la version de build d’Office.</span><span class="sxs-lookup"><span data-stu-id="71deb-312">Replace  *%version%*  with the build version of Office.</span></span> <span data-ttu-id="71deb-313">Cela peut être dérivé des métadonnées de mise à jour du client (décrit dans la section suivante).</span><span class="sxs-lookup"><span data-stu-id="71deb-313">This can be derived from the Client Update metadata (explained in the next section).</span></span> 
    
- <span data-ttu-id="71deb-314">Définissez *baseURL* à l’aide de la valeur d’URL associée à la branche pour laquelle l’image est créée.</span><span class="sxs-lookup"><span data-stu-id="71deb-314">Define  *baseURL*  by using the URL value associated with the branch the image is being created for.</span></span> <span data-ttu-id="71deb-315">Il est dérivé des métadonnées de mise à jour du client, comme indiqué dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="71deb-315">This is derived from the Client Update metadata, explained in the following section.</span></span> 
    
<span data-ttu-id="71deb-316">Les étapes de création d’une image sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="71deb-316">The steps for creating an image are:</span></span>
  
1. <span data-ttu-id="71deb-317">Ouvrez la liste des fichiers XML.</span><span class="sxs-lookup"><span data-stu-id="71deb-317">Open the XML file list.</span></span>
    
2. <span data-ttu-id="71deb-318">Remplacez les occurrences de *% version%* par la version de build Office applicable.</span><span class="sxs-lookup"><span data-stu-id="71deb-318">Replace occurrences of  *%version%*  with the applicable Office build version.</span></span> <span data-ttu-id="71deb-319">La version de build peut être obtenue à partir de releasehistory. xml, comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="71deb-319">The build version can be acquired from releasehistory.xml as described later in this article.</span></span> 
    
3. <span data-ttu-id="71deb-320">Lisez l’attribut URL de la branche cible.</span><span class="sxs-lookup"><span data-stu-id="71deb-320">Read the URL attribute for the target branch.</span></span>
    
4. <span data-ttu-id="71deb-321">Supprimez les nœuds de langue pour toutes les langues non requises dans l’image personnalisée.</span><span class="sxs-lookup"><span data-stu-id="71deb-321">Remove language nodes for any languages not required in the custom image.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="71deb-322">Les nœuds avec la langue = ' 0 'sont neutres pour la langue et doivent être inclus dans l’image.</span><span class="sxs-lookup"><span data-stu-id="71deb-322">Nodes with language='0' are language neutral and must be included in the image.</span></span> 
  
5. <span data-ttu-id="71deb-323">Construisez une image locale du CDN en itérant dans la liste de fichiers XML et en copiant les fichiers CDN, lors de la création de la structure de dossiers selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="71deb-323">Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed.</span></span> 
    
   - <span data-ttu-id="71deb-324">Si l’attribut *Rename* est fourni, *renommez* le fichier copié avec la valeur fournie dans l’attribut Rename.</span><span class="sxs-lookup"><span data-stu-id="71deb-324">If the  *rename*  attribute is provided, then  *rename*  the copied file to the value provided in the rename attribute.</span></span> <span data-ttu-id="71deb-325">Il est utilisé pour créer les fichiers V64. cab et V32. cab de niveau supérieur par défaut.</span><span class="sxs-lookup"><span data-stu-id="71deb-325">This is used to create the top-level default v64.cab and v32.cab files.</span></span> <span data-ttu-id="71deb-326">Il s’agit des versions renommées du fichier CAB de build de niveau supérieur, qui sont utilisées comme version d’installation par défaut si la version n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="71deb-326">These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified.</span></span> 
    
   - <span data-ttu-id="71deb-327">Utilisez URL + relativePath + nom de fichier pour construire l’emplacement du CDN.</span><span class="sxs-lookup"><span data-stu-id="71deb-327">Use URL + relativePath + filename to construct the CDN location.</span></span>
    
<span data-ttu-id="71deb-328">Voici des exemples qui utilisent le canal mensuel (tel que défini par le `<baseURL>` nœud) et Build version 16.0.4229.1004 à partir de releasehistory. Xml.</span><span class="sxs-lookup"><span data-stu-id="71deb-328">The following are examples that use the Monthly channel (as defined by the  `<baseURL>` node) and build version 16.0.4229.1004 from releasehistory.xml.</span></span> 
  
```xml
<baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- <span data-ttu-id="71deb-329">Voici un fichier indépendant de la langue nécessaire pour toutes les langues.</span><span class="sxs-lookup"><span data-stu-id="71deb-329">The following is a language neutral file needed for all languages.</span></span> <span data-ttu-id="71deb-330">Le nom du fichier est v64_16.0.4229.1004. cab et doit être copié à partir de `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` et renommé `…/office/data/v64.cab`.</span><span class="sxs-lookup"><span data-stu-id="71deb-330">The name of the file is v64_16.0.4229.1004.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` and renamed to `…/office/data/v64.cab`.</span></span> 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- <span data-ttu-id="71deb-331">Vous trouverez ci-dessous un fichier à inclure dans l’image en-US, comme indiqué par le LCID de langue = 1033.</span><span class="sxs-lookup"><span data-stu-id="71deb-331">The following is a file to be included in the en-US image as designated by the language LCID=1033.</span></span> <span data-ttu-id="71deb-332">Le nom du fichier est s641033. cab et doit être copié à partir de `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` et non renommé.</span><span class="sxs-lookup"><span data-stu-id="71deb-332">The name of the file is s641033.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` and not renamed.</span></span>
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="71deb-333">Vérification de hachage des fichiers. dat</span><span class="sxs-lookup"><span data-stu-id="71deb-333">Hash verification of .dat files</span></span>

<span data-ttu-id="71deb-334">Les outils de création d’image peuvent vérifier l’intégrité des fichiers. dat téléchargés en comparant une valeur de hachage calculée avec la valeur de hachage fournie associée à chacun des fichiers. dat.</span><span class="sxs-lookup"><span data-stu-id="71deb-334">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files.</span></span> <span data-ttu-id="71deb-335">Voici un exemple de fichier. dat du canal mensuel avec Build version 16.0.4229.1004 et langue définie sur bulgare :</span><span class="sxs-lookup"><span data-stu-id="71deb-335">Following is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian:</span></span>
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- <span data-ttu-id="71deb-336">L’attribut **hashLocation** spécifie l’emplacement de chemin d’accès relatif du Stream.x64.BG-BG. Hash pour le fichier Stream.x64.BG-BG. dat.</span><span class="sxs-lookup"><span data-stu-id="71deb-336">The **hashLocation** attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file.</span></span> <span data-ttu-id="71deb-337">Construisez l’emplacement du fichier de hachage en concaténant URL + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="71deb-337">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="71deb-338">Dans l’exemple suivant, l’emplacement stream.x64.bg-bg. hash doit être :</span><span class="sxs-lookup"><span data-stu-id="71deb-338">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="71deb-339">L’attribut **hashAlgo** spécifie l’algorithme de hachage qui a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="71deb-339">The **hashAlgo** attribute specifies what hashing algorithm was used.</span></span> <span data-ttu-id="71deb-340">Dans ce cas, SHA256 a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="71deb-340">In this case Sha256 was used.</span></span> 
    
  <span data-ttu-id="71deb-341">Pour valider l’intégrité du fichier stream.x64.bg-bg. dat, ouvrez stream.x64.bg-bg. Hash et lisez la valeur de hachage qui est la première ligne de texte dans le fichier de hachage.</span><span class="sxs-lookup"><span data-stu-id="71deb-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="71deb-342">Comparez ceci à la valeur de hachage calculée (à l’aide de l’algorithme de hachage spécifié) pour vérifier l’intégrité du fichier. dat téléchargé.</span><span class="sxs-lookup"><span data-stu-id="71deb-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="71deb-343">L’exemple suivant montre le code C# permettant de lire le hachage.</span><span class="sxs-lookup"><span data-stu-id="71deb-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a><span data-ttu-id="71deb-344">Mises à jour du client Office 365</span><span class="sxs-lookup"><span data-stu-id="71deb-344">Office 365 Client Updates</span></span>

<span data-ttu-id="71deb-345">Toutes les mises à jour du client Office 365 sont publiées dans le [catalogue Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="71deb-345">All Office 365 Client Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="71deb-346">Les mises à jour du client Office 365 permettent aux logiciels de gérabilité de traiter les mises à jour du client Office 365 de manière très similaire à toute autre mise à jour WU, à une exception près : les mises à jour du client ne contiennent pas de charge utile réelle.</span><span class="sxs-lookup"><span data-stu-id="71deb-346">Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="71deb-347">Les mises à jour du client Office 365 ne doivent pas être installées sur les clients, mais plutôt utilisées pour déclencher les flux de travail avec le logiciel de gérabilité en remplaçant la commande d’installation par le mécanisme d’installation basé sur COM indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="71deb-347">The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span> 
  
<span data-ttu-id="71deb-348">**La figure suivante illustre un diagramme du flux de travail de mise à jour du client Office 365.**</span><span class="sxs-lookup"><span data-stu-id="71deb-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="71deb-349">![Diagramme de flux de travail pour les mises à jour du client O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagramme de flux de travail pour les mises à jour du client O365PP")</span><span class="sxs-lookup"><span data-stu-id="71deb-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="71deb-350">Chaque mise à jour du client Office 365 publiée inclut des métadonnées sur la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-350">Each Office 365 Client Update that is published includes metadata about the update.</span></span> <span data-ttu-id="71deb-351">Ces métadonnées incluent un paramètre nommé *MoreInfoUrl* qui peut être utilisé pour dériver les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="71deb-351">This metadata includes a parameter called  *MoreInfoUrl*  which can be used to derive the following information:</span></span> 
  
-  <span data-ttu-id="71deb-352">*Ver*: identifie la version d’Office associée à cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-352">*Ver*: Identifies the Office version associated with this update.</span></span> 
    
-  <span data-ttu-id="71deb-353">*Branch*: identifie le canal de mise à jour pour cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-353">*Branch*: Identifies the Update Channel for this update.</span></span> <span data-ttu-id="71deb-354">Les valeurs incluent InsiderFast, Insiders, Monthly, Targeted, large.</span><span class="sxs-lookup"><span data-stu-id="71deb-354">Values include InsiderFast, Insiders, Monthly, Targeted, Broad.</span></span> <span data-ttu-id="71deb-355">Des valeurs supplémentaires peuvent être ajoutées à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="71deb-355">Additional values may be added in the future.</span></span> 
    
-  <span data-ttu-id="71deb-356">*ARCH*: identifie l’architecture de processeur associée à cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-356">*Arch*: Identifies the processor architecture associated with this update.</span></span> 
    
-  <span data-ttu-id="71deb-357">*xmlVer*: version des listes de fichiers XML qui doivent être utilisées pour construire l’image de base pour cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-357">*xmlVer*: The version of the XML file lists that should be used to construct the base image for this update.</span></span> 
    
-  <span data-ttu-id="71deb-358">*xmlpath*: chemin d’accès au OFL. CAB qui contient les listes de fichiers XML.</span><span class="sxs-lookup"><span data-stu-id="71deb-358">*xmlPath*: Path to the OFL.CAB file which contains the XML file lists.</span></span> 
    
-  <span data-ttu-id="71deb-359">*mlFile*: nom de la liste de fichiers qui doit être utilisée pour cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="71deb-359">*mlFile*: The name of the file list that should be used for this update.</span></span> <span data-ttu-id="71deb-360">La valeur sera O365Client_32bit ou O365Client_64bit et correspondra à l’Arch.</span><span class="sxs-lookup"><span data-stu-id="71deb-360">The value will be O365Client_32bit or O365Client_64bit and will match the Arch.</span></span> 
    
<span data-ttu-id="71deb-361">L’URL suivante est un exemple du paramètre *MoreInfoURL* qui se réfère aux versions de mise à jour du client Office 365 pour la version 32 bits d’Office avec la version de build de 16.0.2342.2343 sur le canal actuel.</span><span class="sxs-lookup"><span data-stu-id="71deb-361">The following URL is an example of the  *MoreInfoURL*  parameter which refers to the Office 365 client update releases for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel.</span></span> 
  
<span data-ttu-id="71deb-362">https://officecdn.microsoft.com/pr/wsus/ofl.cabest l’emplacement des listes de fichiers XML pour cette mise à jour, en particulier le O365Client_32bit. XML à partir du OFL. Taxi.</span><span class="sxs-lookup"><span data-stu-id="71deb-362">https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.</span></span>
  
[<span data-ttu-id="71deb-363">Versions du canal de mise à jour du client Office 365</span><span class="sxs-lookup"><span data-stu-id="71deb-363">Office 365 client update channel releases</span></span>](https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="71deb-364">Métadonnées supplémentaires pour l’automatisation du transfert de contenu</span><span class="sxs-lookup"><span data-stu-id="71deb-364">Additional metadata for automating content staging</span></span>

<span data-ttu-id="71deb-365">En plus des métadonnées qui sont publiées, qui définit des fichiers XML supplémentaires publiés sur le CDN, qui peuvent vous aider à fournir des informations supplémentaires sur les clients Office 365 disponibles à partir du CDN Office.</span><span class="sxs-lookup"><span data-stu-id="71deb-365">In addition to the metadata that is published which defines there are also additional XML files published to the CDN that can help provide additional information about the Office 365 clients that are available from the Office CDN.</span></span>
  
<span data-ttu-id="71deb-366">**SKU. LANGAGE**</span><span class="sxs-lookup"><span data-stu-id="71deb-366">**SKUS.XML**</span></span>
  
<span data-ttu-id="71deb-367">Ce fichier XML est inclus dans un fichier CAB signé et publié sur le CDN Office à l’URL suivante [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab):.</span><span class="sxs-lookup"><span data-stu-id="71deb-367">This XML file is contained within a signed CAB and published to the Office CDN at the following URL: [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab).</span></span>
  
<span data-ttu-id="71deb-368">Les métadonnées publiées dans ce fichier XML sont utiles pour déterminer les produits disponibles pour le déploiement et la maintenance à partir du CDN Office, ainsi que diverses options pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="71deb-368">The metadata published in this XML file is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseInfo PublishedDate="08/07/2017 16:34">
  <!-- Suite / App catalog -->
  <Suite>
    <SKU Name="Office 365 ProPlus" ProductID="O365ProPlusRetail" Default="True">
      <Apps>
        <App Name="Access" AppID="Access" />
        <App Name="Excel" AppID="Excel" />
        <App Name="OneDrive for Business (Groove)" AppID="Groove" />
        <App Name="OneDrive for Business (Next Gen Sync Client)" AppID="OneDrive" />
        <App Name="OneNote" AppID="OneNote" />
        <App Name="Outlook" AppID="Outlook" />
        <App Name="PowerPoint" AppID="PowerPoint" />
        <App Name="Publisher" AppID="Publisher" />
        <App Name="Skype for Business" AppID="Lync" />
        <App Name="Word" AppID="Word" />
      </Apps>
      <Channels>
        <Channel ID="Monthly"/>
        <Channel ID="Insiders"/>
        <Channel ID="Targeted"/>
        <Channel ID="Broad"/>
      </Channels>
    </SKU>
```

<span data-ttu-id="71deb-369">Le nœud racine **ReleaseInfo\> contient l’attribut PublishedDate qui identifie la date à laquelle ce fichier a été publié. \<**</span><span class="sxs-lookup"><span data-stu-id="71deb-369">**\<ReleaseInfo\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="71deb-370">Le nœud **SKU\> identifie une UGS individuelle. \<**</span><span class="sxs-lookup"><span data-stu-id="71deb-370">**\<SKU\>** node identifies an individual SKU.</span></span> 
  
- <span data-ttu-id="71deb-371">L’attribut *ProductID* identifie l’ID transmis en tant qu’attribut ID dans le fichier Configuration. XML en cas d’utilisation de l’outil odt.</span><span class="sxs-lookup"><span data-stu-id="71deb-371">The  *ProductID*  attribute identifies the ID that is passed as the ID attribute in the configuration.xml if using the ODT.</span></span> <span data-ttu-id="71deb-372">Par exemple, `<Product ID="O365ProPlusRetail">`.</span><span class="sxs-lookup"><span data-stu-id="71deb-372">For example, `<Product ID="O365ProPlusRetail">`.</span></span> 
    
- <span data-ttu-id="71deb-373">L’attribut *par défaut* , s’il est défini sur true, identifie la référence recommandée.</span><span class="sxs-lookup"><span data-stu-id="71deb-373">The  *Default*  attribute, if set to True, identifies the recommended SKU.</span></span> 
    
<span data-ttu-id="71deb-374">Les nœuds d' **application\> sont utilisés pour définir les applications Office individuelles prises en charge par chaque SKU. \<**</span><span class="sxs-lookup"><span data-stu-id="71deb-374">**\<App\>** nodes are used to define the individual Office apps that each SKU supports.</span></span> 
  
- <span data-ttu-id="71deb-375">L’attribut *Name* est le nom de l’application affichée.</span><span class="sxs-lookup"><span data-stu-id="71deb-375">The  *Name*  attribute is the displayed application name.</span></span> 
    
- <span data-ttu-id="71deb-376">L’attribut *AppID* est l’attribut ID transmis dans le fichier Configuration. xml pour \*\* \<le\> nœud ExcludeApp\*\* si vous utilisez l’outil odt.</span><span class="sxs-lookup"><span data-stu-id="71deb-376">The  *AppID*  attribute is the ID attribute passed in the configuration.xml for the **\<ExcludeApp\>** node if using the ODT.</span></span> <span data-ttu-id="71deb-377">Par exemple, `<ExcludeApp ID="Publisher" />`.</span><span class="sxs-lookup"><span data-stu-id="71deb-377">For example, `<ExcludeApp ID="Publisher" />`.</span></span> 
    
<span data-ttu-id="71deb-378">**RELEASEHISTORY. LANGAGE**</span><span class="sxs-lookup"><span data-stu-id="71deb-378">**RELEASEHISTORY.XML**</span></span>
  
<span data-ttu-id="71deb-379">Ce fichier XML est inclus dans un fichier CAB signé et publié sur le CDN Office à l’emplacement suivant [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab):.</span><span class="sxs-lookup"><span data-stu-id="71deb-379">This XML file is contained within a signed CAB and published to the Office CDN at the following location: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span></span> 
  
<span data-ttu-id="71deb-380">Les métadonnées publiées dans ce fichier XML sont utiles pour déterminer les canaux pris en charge pour la maintenance des mises à jour à partir du CDN Office, ainsi que des informations sur l’historique de build de chacun des canaux pris en charge.</span><span class="sxs-lookup"><span data-stu-id="71deb-380">The metadata published in this XML file is useful for determining which channels are supported for servicing updates from the Office CDN along with information about the build history for each of the supported channels.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseHistory PublishedDate="10/22/2017 00:48">
  <UpdateChannel Name="Current" ID="Monthly" DisplayName="Monthly Channel">
    <Update Latest="True" Version="1709" LegacyVersion="16.0.8528.2139" Build="8528.2139" PubTime="2017-10-16T19:45:50.743Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2107" Build="8431.2107" PubTime="2017-10-11T01:52:33.793Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2079" Build="8431.2079" PubTime="2017-09-18T22:26:13.673Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2107" Build="8326.2107" PubTime="2017-09-12T18:56:53.657Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2096" Build="8326.2096" PubTime="2017-08-30T00:10:25.253Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2076" Build="8326.2076" PubTime="2017-08-19T00:13:01.787Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2073" Build="8326.2073" PubTime="2017-08-11T19:35:42.173Z" />
  </UpdateChannel>
```

<span data-ttu-id="71deb-381">Le nœud racine \*\* \<ReleaseHistory\> \*\* contient l’attribut PublishedDate qui identifie la date à laquelle ce fichier a été publié.</span><span class="sxs-lookup"><span data-stu-id="71deb-381">The **\<ReleaseHistory\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="71deb-382">Le \*\* \<nœud\> UpdateChannel\*\* définit un canal pris en charge.</span><span class="sxs-lookup"><span data-stu-id="71deb-382">The **\<UpdateChannel\>** node defines a supported channel.</span></span> 
  
- <span data-ttu-id="71deb-383">L’attribut *Name* définit l’ID de canal qui est utilisé pour transmettre l’outil ODT dans le fichier Configuration. XML en tant qu’attribut Channel.</span><span class="sxs-lookup"><span data-stu-id="71deb-383">The  *Name*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="71deb-384">Exemple : `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span><span class="sxs-lookup"><span data-stu-id="71deb-384">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span></span> 
    
  > [!NOTE] 
  > <span data-ttu-id="71deb-385">Cet attribut a été déconseillé et est utilisé uniquement à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="71deb-385">This attribute has been deprecated and is used for backward compatibility only.</span></span> <span data-ttu-id="71deb-386">Utilisez l’attribut ID à la place de l’attribut Name.</span><span class="sxs-lookup"><span data-stu-id="71deb-386">Use the ID attribute in place of the Name attribute.</span></span> 
    
- <span data-ttu-id="71deb-387">L’attribut *ID* définit l’ID de canal qui est utilisé pour transmettre l’outil ODT dans le fichier Configuration. XML en tant qu’attribut Channel.</span><span class="sxs-lookup"><span data-stu-id="71deb-387">The  *ID*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="71deb-388">Exemple : `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span><span class="sxs-lookup"><span data-stu-id="71deb-388">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span></span> 
    
- <span data-ttu-id="71deb-389">L’attribut **DisplayName** est utilisé comme nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="71deb-389">The **DisplayName**  attribute is used as the display name.</span></span> 
    
<span data-ttu-id="71deb-390">Le nœud de \*\* \<mise à jour\> \*\* est utilisé pour définir chaque mise à jour qui a été publiée pour ce canal particulier.</span><span class="sxs-lookup"><span data-stu-id="71deb-390">The **\<Update\>** node is used to define each update that has been published for that particular channel.</span></span> 
  
- <span data-ttu-id="71deb-391">L’attribut le **plus récent** , s’il est défini sur true, définit la version qui est la dernière version de ce canal.</span><span class="sxs-lookup"><span data-stu-id="71deb-391">The **Latest**  attribute, if set to True, defines the release that is the latest release for that channel.</span></span> 
    
- <span data-ttu-id="71deb-392">L’attribut **version** définit le numéro de version de cette mise à jour particulière.</span><span class="sxs-lookup"><span data-stu-id="71deb-392">The **Version** attribute defines the version number for this particular update.</span></span> 
    
- <span data-ttu-id="71deb-393">L’attribut **LegacyVersion** définit le numéro de version complet de cette mise à jour particulière.</span><span class="sxs-lookup"><span data-stu-id="71deb-393">The **LegacyVersion** attribute defines the full version number for this particular update.</span></span> 
    
- <span data-ttu-id="71deb-394">L’attribut **Build** définit le numéro de build de cette mise à jour particulière.</span><span class="sxs-lookup"><span data-stu-id="71deb-394">The **Build** attribute defines the build number for this particular update.</span></span> 
    
- <span data-ttu-id="71deb-395">L’attribut **PubTime** définit la date et l’heure de publication de cette mise à jour sur le CDN Office.</span><span class="sxs-lookup"><span data-stu-id="71deb-395">The **PubTime** attribute defines the date and time at which this update was published to the Office CDN.</span></span> 
    

