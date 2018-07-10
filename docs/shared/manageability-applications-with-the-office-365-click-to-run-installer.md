---
title: Intégration d’applications de gestion avec Office 365 click-to-run installer
manager: kelbow
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Découvrez comment intégrer le programme d’installation Office 365 Click-to-Run avec une solution de gestion de logiciels.
ms.openlocfilehash: abe941e3e3818eed1f18108f1678e46e8156b08c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787943"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a><span data-ttu-id="3548a-103">Intégration d’applications de gestion avec Office 365 click-to-run installer</span><span class="sxs-lookup"><span data-stu-id="3548a-103">Integrating manageability applications with Office 365 click-to-run installer</span></span>

<span data-ttu-id="3548a-104">Découvrez comment intégrer le programme d’installation Office 365 Click-to-Run avec une solution de gestion de logiciels.</span><span class="sxs-lookup"><span data-stu-id="3548a-104">Learn how to integrate the Office 365 Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="3548a-105">Le programme d’installation Office 365 Click-to-Run fournit une interface COM qui permet de contrôler par programme de gestion de la mise à jour professionnels de l’informatique et les solutions de gestion de logiciels.</span><span class="sxs-lookup"><span data-stu-id="3548a-105">The Office 365 Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="3548a-106">Cette interface fournit des fonctions de gestion supplémentaires au-delà de celles fournies par l’outil de déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3548a-107">Cet article s’applique à Office 2016 et versions ultérieures, Office 365.</span><span class="sxs-lookup"><span data-stu-id="3548a-107">This article applies to Office 2016 and later, Office 365.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="3548a-108">Intégration avec Click-to-Run</span><span class="sxs-lookup"><span data-stu-id="3548a-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="3548a-109">Pour utiliser cette interface, une application de gestion appelle l’interface COM et appelle exposé API qui communiquent directement avec le service d’installation Click-to-Run.</span><span class="sxs-lookup"><span data-stu-id="3548a-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3548a-110">Le programme d’installation Office Click-to-Run peut être exécutée à partir de la ligne de commande avec les paramètres qui peuvent contrôler le comportement, comme indiqué dans [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117).</span><span class="sxs-lookup"><span data-stu-id="3548a-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117).</span></span> 
  
<span data-ttu-id="3548a-111">**Voici un diagramme conceptuel de l’interface COM**</span><span class="sxs-lookup"><span data-stu-id="3548a-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="3548a-112">![Un diagramme de l’utilisation de l’interface COM sur le programme d’installation Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Un diagramme de l’utilisation de l’interface COM sur le programme d’installation Office Click-To-Run")</span><span class="sxs-lookup"><span data-stu-id="3548a-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="3548a-113">L’interface implémente com. installer Office 365 Click-to-Run, **IUpdateNotify** inscrit à CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="3548a-113">The Office 365 Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="3548a-114">Cette interface peut être appelée comme suit :</span><span class="sxs-lookup"><span data-stu-id="3548a-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="3548a-115">L’appel réussit uniquement si l’appelant s’exécute avec des privilèges élevés, comme le programme d’installation Click-to-Run doit être exécuté avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="3548a-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="3548a-116">L’interface **IUpdateNotify** COM expose trois fonctions asynchrones responsables de la validation les commandes et paramètres et planification de l’exécution avec le service d’installation Click-to-Run.</span><span class="sxs-lookup"><span data-stu-id="3548a-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="3548a-117">Une autre méthode, **état**, peut être utilisée pour obtenir des informations sur l’état de la dernière commande exécutée ou l’état de la commande en cours d’exécution (succès, échec, les codes d’erreur détaillé).</span><span class="sxs-lookup"><span data-stu-id="3548a-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="3548a-118">Il existe quatre états que le service d’installation Click-to-Run peut prendre au cours de son cycle de vie, pendant laquelle les méthodes **IUpdateNotify** peuvent être appelées ; Redémarrage, inactif, le téléchargement et l’application.</span><span class="sxs-lookup"><span data-stu-id="3548a-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="3548a-119">**Voici le diagramme de la Machine à états Interface COM**</span><span class="sxs-lookup"><span data-stu-id="3548a-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="3548a-120">![Un diagramme d’état de l’interface COM.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Un diagramme d’état de l’interface COM")</span><span class="sxs-lookup"><span data-stu-id="3548a-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="3548a-121">**Redémarrage**: démarrage de l’ordinateur est un certain temps lorsque le service du programme d’installation Click-to-Run n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="3548a-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="3548a-122">Un appel réussi à la méthode état après un redémarrage renverra eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="3548a-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="3548a-123">**Inactif :** Lorsque le programme d’installation Click-to-Run se trouve dans l’état d’inactivité, vous pouvez appeler :</span><span class="sxs-lookup"><span data-stu-id="3548a-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="3548a-124">**Appliquer**: Install déjà téléchargé du contenu.</span><span class="sxs-lookup"><span data-stu-id="3548a-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="3548a-125">**Annuler**: renvoie `0x800000e`, « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="3548a-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="3548a-126">**Télécharger**: télécharge le nouveau contenu pour l’installation du client pour une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3548a-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="3548a-127">**État**: renvoie le résultat de la dernière action terminée, ou un message d’erreur si l’action s’est terminée en échec.</span><span class="sxs-lookup"><span data-stu-id="3548a-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="3548a-128">S’il n’existe aucune action précédente, **état** renvoie `eUPDATE_UNKNOWN`.</span><span class="sxs-lookup"><span data-stu-id="3548a-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="3548a-129">**Téléchargement :** Lorsque le programme d’installation Click-to-Run se trouve dans l’état de téléchargement, vous pouvez appeler :</span><span class="sxs-lookup"><span data-stu-id="3548a-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="3548a-130">**Appliquer**: renvoie une **valeur HRESULT** avec la valeur `0x800000e`, « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="3548a-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="3548a-131">**Annuler**: arrête le téléchargement et supprime le contenu téléchargé partiellement.</span><span class="sxs-lookup"><span data-stu-id="3548a-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="3548a-132">**Télécharger**: renvoie une **valeur HRESULT** avec la valeur `0x800000e`, « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="3548a-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="3548a-133">**État**: renvoie **DOWNLOAD_WIP** pour indiquer que le travail de téléchargement est en cours.</span><span class="sxs-lookup"><span data-stu-id="3548a-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="3548a-134">**Application :** Lorsque le programme d’installation Click-to-Run est en cours d’installation précédemment télécharger du contenu :</span><span class="sxs-lookup"><span data-stu-id="3548a-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="3548a-135">**Appliquer**: renvoie une **valeur HRESULT** avec la valeur `0x800000e`, « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="3548a-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="3548a-136">**Annuler**: renvoie `0x800000e`, l’action Appliquer ne peut pas être annulée.</span><span class="sxs-lookup"><span data-stu-id="3548a-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="3548a-137">**Télécharger**: renvoie une **valeur HRESULT** avec la valeur `0x800000e`, « une méthode a été appelée à un moment inattendu ».</span><span class="sxs-lookup"><span data-stu-id="3548a-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="3548a-138">**État**: renvoie **APPLY_WIP** pour indiquer qui applique le travail est en cours.</span><span class="sxs-lookup"><span data-stu-id="3548a-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="3548a-139">Étant donné que OfficeC2RCOM est un service COM + et est chargé de manière dynamique, vous devez appeler **CoCreateInstance** chaque fois que vous appelez une méthode de cette classe pour vous assurer que vous obtenez le résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="3548a-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="3548a-140">Service COM + gère la création d’une nouvelle instance si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3548a-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="3548a-141">Lorsqu’une des méthodes est appelée pour la première fois, COM + charge l’objet **IUpdateNotify** et exécutez-le dans une des instances de dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="3548a-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="3548a-142">Le nouvel objet restera actif pendant environ 3 minutes dans inactif.</span><span class="sxs-lookup"><span data-stu-id="3548a-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="3548a-143">Si un appel suivant est effectué dans les trois minutes du dernier appel, l’objet **IUpdateNotify** restera chargé et une nouvelle instance n’est pas créée.</span><span class="sxs-lookup"><span data-stu-id="3548a-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="3548a-144">Si aucun appel n’est effectué dans les trois minutes, l’objet IUpdateNotify doit être déchargé et un nouvel objet **IUpdateNotify** sera créé lors de l’appel suivant.</span><span class="sxs-lookup"><span data-stu-id="3548a-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="3548a-145">Guide de référence des API COM Click-to-Run installer</span><span class="sxs-lookup"><span data-stu-id="3548a-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="3548a-146">Dans la documentation de référence API suivante :</span><span class="sxs-lookup"><span data-stu-id="3548a-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="3548a-147">Les paramètres sont dans un format de paire clé/valeur séparée par un espace.</span><span class="sxs-lookup"><span data-stu-id="3548a-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="3548a-148">Les paramètres ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="3548a-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="3548a-149">Il existe une [liste de paramètres](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) avec la documentation disponible.</span><span class="sxs-lookup"><span data-stu-id="3548a-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="3548a-150">Résumé de l’interface IUpdateNotify2 est désormais inclus.</span><span class="sxs-lookup"><span data-stu-id="3548a-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="3548a-151">Appliquer</span><span class="sxs-lookup"><span data-stu-id="3548a-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="3548a-152">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3548a-152">Parameters</span></span>

-  <span data-ttu-id="3548a-153">_DisplayLevel_: **true** pour afficher l’état d’installation, y compris les erreurs, au cours du processus de mise à jour ; **false** pour masquer l’état d’installation, y compris les erreurs, au cours du processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3548a-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="3548a-154">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="3548a-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="3548a-155">_forceappshutdown_: **la valeur true** pour forcer l’archivage des applications Office à arrêter immédiatement l’action **Appliquer** déclenchement ; **false** échoue si toutes les applications Office sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3548a-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="3548a-156">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="3548a-156">The default is **false**.</span></span> <span data-ttu-id="3548a-157">Pour plus d’informations, consultez la [section Notes](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="3548a-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="3548a-158">Si n’importe quelle application Office est en cours d’exécution lors de l’action **Appliquer** est déclenchée, l’action **Appliquer** généralement échoue.</span><span class="sxs-lookup"><span data-stu-id="3548a-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="3548a-159">Transmission `forceappshutdown=true` pour **Appliquer** la méthode provoque le service **OfficeClickToRun** arrêter les applications et appliquer la mise à jour immédiatement.</span><span class="sxs-lookup"><span data-stu-id="3548a-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="3548a-160">L’utilisateur peut rencontrer une perte de données dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="3548a-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="3548a-161">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="3548a-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3548a-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="3548a-162">**S_OK**</span></span> <br/> |<span data-ttu-id="3548a-163">Action a bien été envoyée au service Click-To-Run pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3548a-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="3548a-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="3548a-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="3548a-165">L’appelant n’est pas en cours d’exécution avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="3548a-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="3548a-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="3548a-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="3548a-167">Paramètres non valides ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="3548a-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="3548a-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="3548a-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="3548a-169">Action n’est pas autorisée à ce stade.</span><span class="sxs-lookup"><span data-stu-id="3548a-169">Action is not allowed at this time.</span></span> <span data-ttu-id="3548a-170">Pour plus d’informations, consultez la [section Notes](#bk_ApplyRemark) .</span><span class="sxs-lookup"><span data-stu-id="3548a-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="3548a-171">Remarques</span><span class="sxs-lookup"><span data-stu-id="3548a-171">Remarks</span></span>

- <span data-ttu-id="3548a-172">Si n’importe quelle application Office est en cours d’exécution lors de l’action **Appliquer** est déclenchée, l’action **Appliquer** échouera.</span><span class="sxs-lookup"><span data-stu-id="3548a-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="3548a-173">Transmission `forceappshutdown=true` pour **Appliquer** la méthode provoque le service **OfficeClickToRun** arrêter immédiatement toutes les applications Office qui sont en cours d’exécution et appliquent la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3548a-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="3548a-174">L’utilisateur peut rencontrer données comme ils ne sont pas invités à enregistrer les modifications pour ouvrir des documents...</span><span class="sxs-lookup"><span data-stu-id="3548a-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="3548a-175">Cette action ne peut être déclenchée lorsque le statut COM est une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3548a-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="3548a-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3548a-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="3548a-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="3548a-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="3548a-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="3548a-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="3548a-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="3548a-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="3548a-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="3548a-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="3548a-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="3548a-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="3548a-182">Si vous appelez la méthode **Apply** sans télécharger le contenu précédemment, la méthode **Apply** signalera **réussi** détecté rien à appliquer et réussi le processus à **Appliquer** .</span><span class="sxs-lookup"><span data-stu-id="3548a-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="3548a-183">Cancel</span><span class="sxs-lookup"><span data-stu-id="3548a-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="3548a-184">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="3548a-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3548a-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="3548a-185">S_OK</span></span>  <br/> |<span data-ttu-id="3548a-186">Action a bien été envoyée au service Click-to-Run pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3548a-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="3548a-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="3548a-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="3548a-188">Action n’est pas autorisée à ce stade.</span><span class="sxs-lookup"><span data-stu-id="3548a-188">Action is not allowed at this time.</span></span> <span data-ttu-id="3548a-189">Consultez la section [Notes](#bk_CancelRemarks) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3548a-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="3548a-190">Remarques</span><span class="sxs-lookup"><span data-stu-id="3548a-190">Remarks</span></span>

- <span data-ttu-id="3548a-191">Cette méthode peut uniquement être déclenché lorsque l' id du statut COM **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="3548a-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="3548a-192">Il essaie d’annuler l’opération de téléchargement en cours.</span><span class="sxs-lookup"><span data-stu-id="3548a-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="3548a-193">L’état COM sera Remplacez **eDOWNLOAD_CANCELLING** et finalement à **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="3548a-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="3548a-194">L’état COM renverra **E_ILLEGAL_METHOD_CALL** si déclenché à tout moment.</span><span class="sxs-lookup"><span data-stu-id="3548a-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="3548a-195">Téléchargement</span><span class="sxs-lookup"><span data-stu-id="3548a-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="3548a-196">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3548a-196">Parameters</span></span>

-  <span data-ttu-id="3548a-197">_DisplayLevel_: **true** pour afficher l’état d’installation, y compris les erreurs, au cours du processus de mise à jour ; **false** pour masquer l’état d’installation, y compris les erreurs, au cours du processus de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3548a-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="3548a-198">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="3548a-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="3548a-199">_updatebaseurl_: URL de la source de téléchargement de substitution.</span><span class="sxs-lookup"><span data-stu-id="3548a-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="3548a-200">_updatetoversion_: la version mise à jour Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="3548a-201">Définissez ce paramètre si vous souhaitez mettre à jour vers une version antérieure à la version actuellement installée.</span><span class="sxs-lookup"><span data-stu-id="3548a-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="3548a-202">_downloadsource_: le CLSID de l’implémentation de **IBackgroundCopyManager** personnalisé (Gestionnaire de BITS).</span><span class="sxs-lookup"><span data-stu-id="3548a-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="3548a-203">_contentid_: identifie le contenu à télécharger à partir du serveur de contenu via le Gestionnaire de BITS personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3548a-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="3548a-204">Cette valeur est transmise par le biais de l’interface de BITS pour interprétation.</span><span class="sxs-lookup"><span data-stu-id="3548a-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="3548a-205">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="3548a-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3548a-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="3548a-206">**S_OK**</span></span> <br/> |<span data-ttu-id="3548a-207">Action a bien été envoyée au service Click-To-Run pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3548a-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="3548a-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="3548a-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="3548a-209">L’appelant n’est pas en cours d’exécution avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="3548a-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="3548a-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="3548a-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="3548a-211">Paramètres non valides ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="3548a-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="3548a-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="3548a-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="3548a-213">Action n’est pas autorisée à ce stade.</span><span class="sxs-lookup"><span data-stu-id="3548a-213">Action is not allowed at this time.</span></span> <span data-ttu-id="3548a-214">Pour plus d’informations, consultez la [section Notes](#bk_DownloadRemark) .</span><span class="sxs-lookup"><span data-stu-id="3548a-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="3548a-215">Remarques</span><span class="sxs-lookup"><span data-stu-id="3548a-215">Remarks</span></span>

- <span data-ttu-id="3548a-216">Vous devez spécifier _downloadsource_ et _contentid_ comme une paire.</span><span class="sxs-lookup"><span data-stu-id="3548a-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="3548a-217">Si ce n’est pas le cas, la méthode **Télécharger** renverra une erreur **E_INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="3548a-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="3548a-218">Si _downloadsource_, _contentid_et _updatebaseurl_ sont fournis, _updatebaseurl_ sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="3548a-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="3548a-219">Cette action ne peut être déclenchée lorsque le statut COM est une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3548a-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="3548a-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="3548a-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="3548a-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="3548a-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="3548a-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="3548a-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="3548a-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="3548a-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="3548a-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="3548a-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="3548a-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="3548a-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="3548a-226">Si vous appelez la méthode **Apply** sans contenu téléchargé précédemment, la méthode **Apply** signalera **réussi** détecté rien à appliquer et réussi le processus à **Appliquer** .</span><span class="sxs-lookup"><span data-stu-id="3548a-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="3548a-227">Exemples</span><span class="sxs-lookup"><span data-stu-id="3548a-227">Examples</span></span>

- <span data-ttu-id="3548a-228">Pour télécharger le contenu à partir du Gestionnaire de BITS personnalisé : appelez la fonction **download()** en passant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="3548a-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="3548a-229">Pour télécharger le contenu à partir du CDN Microsoft : appelez la fonction **download()** sans spécifier les paramètres _downloadsource_, _contentid_ou _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="3548a-229">To download the content from the Microsoft CDN: Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="3548a-230">Pour télécharger le contenu à partir d’un emplacement personnalisé : appelez la fonction **download()** en passant le paramètre suivant :</span><span class="sxs-lookup"><span data-stu-id="3548a-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="3548a-231">État</span><span class="sxs-lookup"><span data-stu-id="3548a-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="3548a-232">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3548a-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="3548a-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="3548a-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="3548a-234">Pointeur vers une structure UPDATE_STATUS_REPORT.</span><span class="sxs-lookup"><span data-stu-id="3548a-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="3548a-235">Renvoyer des résultats</span><span class="sxs-lookup"><span data-stu-id="3548a-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3548a-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="3548a-236">**S_OK**</span></span> <br/> |<span data-ttu-id="3548a-237">La méthode **Status** renvoie toujours ce résultat.</span><span class="sxs-lookup"><span data-stu-id="3548a-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="3548a-238">Inspecter les `UPDATE_STATUS_RESULT` structure de l’état de l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="3548a-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="3548a-239">Remarques</span><span class="sxs-lookup"><span data-stu-id="3548a-239">Remarks</span></span>

- <span data-ttu-id="3548a-240">Le champ État de la `UPDATE_STATUS_REPORT` contient l’état de l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="3548a-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="3548a-241">Une des valeurs d’état suivant est retournée :</span><span class="sxs-lookup"><span data-stu-id="3548a-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="3548a-242">Si la dernière commande a provoqué une erreur, le champ d’erreur de le `UPDATE_STATUS_REPORT` contient des informations détaillées sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="3548a-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="3548a-243">Deux types de codes d’erreur sont renvoyés à partir de la méthode **d’état** .</span><span class="sxs-lookup"><span data-stu-id="3548a-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="3548a-244">Si l’erreur inférieure à `UDPATE_ERROR_CODE::eUNKNOWN`, l’erreur est un des codes d’erreur prédéfinis suivants :</span><span class="sxs-lookup"><span data-stu-id="3548a-244">If the error less than  `UDPATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="3548a-245">Si le code d’erreur retourné est supérieur à `UDPATE_ERROR_CODE::eUNKNOWN` il s’agit d’un appel de fonction qui a échoué **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3548a-245">If the return error code is larger than  `UDPATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="3548a-246">Pour extraire le HRESULT soustraire `UDPATE_ERROR_CODE::eUNKNOWN` à partir de la valeur renvoyée dans le champ d’erreur de le `UPDATE_STATUS_REPORT`.</span><span class="sxs-lookup"><span data-stu-id="3548a-246">To extract the HRESULT subtract  `UDPATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="3548a-247">La liste complète des valeurs d’erreur et d’état sont consultables en examinant la bibliothèque de type **IUpdateNotify** incorporée dans OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="3548a-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="3548a-248">Le champ contentid est utilisé pour les appels à **l’état** après **téléchargé** a lancé et renvoie le contentid qui a été passé à l’appel à **Télécharger** .</span><span class="sxs-lookup"><span data-stu-id="3548a-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="3548a-249">Il est recommandé d’initialiser ce champ **null** avant d’appeler la méthode **Status** et puis vérifiez la valeur une fois que **l’état** a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="3548a-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="3548a-250">Si la valeur est toujours **null**, qui signifie qu’il n’existe aucune contentid à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="3548a-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="3548a-251">Si la valeur n’est pas **null**, vous devez le libérer avec un appel à **SysFreeString()**.</span><span class="sxs-lookup"><span data-stu-id="3548a-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="3548a-252">Voici un extrait de code d’appel **d’état** après le **téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="3548a-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="3548a-253">Résumé de l’interface IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="3548a-253">Summary of IUpdateNotify2 interface</span></span>

> [!NOTE]
> <span data-ttu-id="3548a-254">Ce résumé est fourni en tant que les informations de complément pour [intégrer la gestion des applications avec le programme d’installation Office 365-un clic](https://msdn.microsoft.com/fr-fr/library/office/mt608768.aspx).</span><span class="sxs-lookup"><span data-stu-id="3548a-254">This summary is provided as a compliment info to [Integrating manageability applications with the Office 365 click-to-run installer](https://msdn.microsoft.com/fr-fr/library/office/mt608768.aspx).</span></span> <span data-ttu-id="3548a-255">Une fois que le document public est mis à jour, ce document peut être considéré comme obsolète.</span><span class="sxs-lookup"><span data-stu-id="3548a-255">Once the public doc is updated, this doc can be considered as obsolete.</span></span> 
  
<span data-ttu-id="3548a-256">À partir de C2RTenant [16.0.8208.6352](http://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (première version accessible au public doit être build de diriger juin--8326.\*), nous avons ajouté une nouvelle interface **IUpdateNotify2** .</span><span class="sxs-lookup"><span data-stu-id="3548a-256">From C2RTenant [16.0.8208.6352](http://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (First publicly available build should be June fork build -- 8326.\*) we have added a new **IUpdateNotify2** interface.</span></span> <span data-ttu-id="3548a-257">Voici certaines informations de base sur cette interface :</span><span class="sxs-lookup"><span data-stu-id="3548a-257">Here is some basic info about this interface:</span></span> 
  
- <span data-ttu-id="3548a-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="3548a-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="3548a-259">Cette interface hébergée également l’interface IUpdateNotify d’origine pour des raisons de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="3548a-259">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="3548a-260">Ce qui signifie que si vous utilisez cette interface, vous avez accès à toutes les méthodes fournies dans l’interface **UpdateNotifyObject** .</span><span class="sxs-lookup"><span data-stu-id="3548a-260">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="3548a-261">Nouvelles méthodes ajoutées à IUpdateNotify2 :</span><span class="sxs-lookup"><span data-stu-id="3548a-261">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="3548a-262">**HRESULT** GetBlockingApps ([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="3548a-262">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="3548a-263">Obtenir des mises à jour de la liste des applications de blocage.</span><span class="sxs-lookup"><span data-stu-id="3548a-263">Get updates blocking apps list.</span></span> <span data-ttu-id="3548a-264">Cet appel renverra les applications Office en cours d’exécution qui bloquent le processus de mise à jour de continuer.</span><span class="sxs-lookup"><span data-stu-id="3548a-264">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="3548a-265">**HRESULT** GetOfficeDeploymentData ([in] type de données int, [in] pcwszName **LPCWSTR** , [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="3548a-265">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="3548a-266">Obtenir les données de déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-266">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="3548a-267">Si vous souhaitez utiliser les nouvelles méthodes, vous devez vous assurer :</span><span class="sxs-lookup"><span data-stu-id="3548a-267">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="3548a-268">Votre version C2R est plus récente que la version ci-dessus (\>= juin diriger version).</span><span class="sxs-lookup"><span data-stu-id="3548a-268">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="3548a-269">Utilisez UpdateNotifyObject2, au lieu **UpdateNotifyObject** pour appeler **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="3548a-269">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="3548a-270">Si vous n’utilisez pas les nouvelles méthodes, vous n’avez pas besoin pour les modifier.</span><span class="sxs-lookup"><span data-stu-id="3548a-270">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="3548a-271">Toutes les méthodes existants fonctionnera exactement la même manière qu’avant.</span><span class="sxs-lookup"><span data-stu-id="3548a-271">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="3548a-272">Implémentation de l’interface de BITS</span><span class="sxs-lookup"><span data-stu-id="3548a-272">Implementing the BITS interface</span></span>

<span data-ttu-id="3548a-273">Le [Service Background Intelligent Transfer Service](https://msdn.microsoft.com/fr-fr/library/bb968799(v=vs.85).aspx) (BITS) est un service fourni par Microsoft pour transférer des fichiers entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="3548a-273">The [Background Intelligent Transfer Service](https://msdn.microsoft.com/fr-fr/library/bb968799(v=vs.85).aspx) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="3548a-274">BITS est un des canaux de programme d’installation Office Click-To-Run permettre utiliser pour télécharger le contenu.</span><span class="sxs-lookup"><span data-stu-id="3548a-274">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="3548a-275">Par défaut, le Office Click-To-Run programme d’installation utilise Windows créées dans l’implémentation de BITS pour télécharger le contenu à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="3548a-275">By default, the Office Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="3548a-276">En fournissant une implémentation personnalisée de BITS à la méthode **download()** de l’interface **IUpdateNotify** , votre logiciel de gestion peut contrôler où et comment le client télécharge le contenu.</span><span class="sxs-lookup"><span data-stu-id="3548a-276">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="3548a-277">Une interface de BITS personnalisée est utile lorsque vous fournissez un canal de distribution de contenu personnalisés autres que les canaux intégrés Click-to-Run, tel que du CDN Office, serveurs IIS, ou les partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3548a-277">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the Office CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="3548a-278">La configuration minimale requise pour une interface personnalisée de BITS fonctionner avec Office C2R service est :</span><span class="sxs-lookup"><span data-stu-id="3548a-278">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="3548a-279">Pour **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="3548a-279">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="3548a-280">Pour **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="3548a-280">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="3548a-281">Pour **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="3548a-281">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="3548a-282">Pour le `Addfile` et `AddFileWithRanges` fonctions, l’URL à distance est au format suivant :</span><span class="sxs-lookup"><span data-stu-id="3548a-282">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="3548a-283">cmbits est codé en dur et signifie BITS personnalisées.</span><span class="sxs-lookup"><span data-stu-id="3548a-283">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="3548a-284">_ \<contentid\> _ est le paramètre _contentid_ pour la méthode **Download()** .</span><span class="sxs-lookup"><span data-stu-id="3548a-284">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="3548a-285">_ \<chemin d’accès relatif au fichier cible\> _ fournit le nom de fichier et emplacement du fichier à télécharger.</span><span class="sxs-lookup"><span data-stu-id="3548a-285">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="3548a-286">Par exemple, si vous avez fourni une _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` à la **Download()** méthode et C2R Office souhaite télécharger le fichier cab de version, tel que `v32.cab` fichier, il appelle **AddFile()** par ce qui suit `RemoteUrl`:</span><span class="sxs-lookup"><span data-stu-id="3548a-286">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="3548a-287">Pour **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="3548a-287">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="3548a-288">Pour **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="3548a-288">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://support.office.com/fr-fr/article/Overview-of-update-channels-for-Office-365-ProPlus-9ccf0f13-28ff-4975-9bd2-7e4ea2fefef4?ui=en-US&rs=en-US&ad=US) using the [Office 2016 Deployment Tool](https://www.microsoft.com/en-us/download/details.aspx?id=49117) or [System Center Configuration Manager](https://support.office.com/fr-fr/article/Manage-updates-to-Office-365-ProPlus-with-System-Center-Configuration-Manager-b4a17328-fcfe-40bf-9202-58d7cbf1cede).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
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
baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="http://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
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
http://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a><span data-ttu-id="3548a-289">Automatisation de test de contenu</span><span class="sxs-lookup"><span data-stu-id="3548a-289">Automating content staging</span></span>

<span data-ttu-id="3548a-290">Les administrateurs informatiques peuvent choisir pour que les clients de bureau configurés pour recevoir des mises à jour automatiquement lorsqu’elles sont disponibles directement à partir de la Microsoft réseau CDN (Content Delivery), ou ils peuvent choisir de contrôler le déploiement des mises à jour disponibles à partir de la mise à jour canaux à l’aide de l’outil de déploiement Office ou System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3548a-290">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or System Center Configuration Manager.</span></span>
  
<span data-ttu-id="3548a-291">Le service prend en charge la possibilité pour les outils de gestion pour qu’il reconnaisse et automatiser le téléchargement du contenu lors de mises à jour sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="3548a-291">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="3548a-292">**L’image suivante est une vue d’ensemble de télécharger une image personnalisée**</span><span class="sxs-lookup"><span data-stu-id="3548a-292">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="3548a-293">![Un diagramme de l’utilisation de l’interface COM sur le programme d’installation Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Un diagramme de l’utilisation de l’interface COM sur le programme d’installation Office Click-To-Run")</span><span class="sxs-lookup"><span data-stu-id="3548a-293">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="3548a-294">Vue d’ensemble de télécharger une image personnalisée</span><span class="sxs-lookup"><span data-stu-id="3548a-294">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="3548a-295">Dans le diagramme précédent, vous voyez qu’une nouvelle image d’Office 365 ProPlus est disponible sur le réseau de Distribution contenu (CDN) Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-295">In the previous diagram, you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN).</span></span> <span data-ttu-id="3548a-296">Avec l’image d’Office 365 ProPlus, une liste de fichiers au format XML est également disponible qui contient les informations nécessaires pour activer le logiciel de gestion créer directement des images personnalisées en remplaçant la nécessité d’utiliser l’outil de déploiement d’Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-296">Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>
  
<span data-ttu-id="3548a-297">Une entreprise configure leurs WSUS pour synchroniser les mises à jour de Client Office 365.</span><span class="sxs-lookup"><span data-stu-id="3548a-297">An enterprise configures their WSUS to sync the Office 365 Client Updates.</span></span> <span data-ttu-id="3548a-298">Ces mises à jour ne contiennent pas de la charge utile réelle de l’image, mais n’autorise pas le logiciel de gestion reconnaître lorsque le nouveau contenu est disponible.</span><span class="sxs-lookup"><span data-stu-id="3548a-298">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="3548a-299">Le logiciel de gestion peut ensuite lire les métadonnées de mise à jour du Client pour comprendre de quelle version d’Office que la mise à jour s’applique à.</span><span class="sxs-lookup"><span data-stu-id="3548a-299">The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.</span></span>
  
<span data-ttu-id="3548a-300">Si la mise à jour est applicable, le logiciel de gestion permettre utiliser le contenu CDN et la liste des fichiers pour créer l’image personnalisée et le stocker sur l’emplacement de partage de fichiers est configuré pour utiliser.</span><span class="sxs-lookup"><span data-stu-id="3548a-300">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="format-of-the-xml-file-list"></a><span data-ttu-id="3548a-301">Format de la liste des fichiers XML</span><span class="sxs-lookup"><span data-stu-id="3548a-301">Format of the XML file list</span></span>

<span data-ttu-id="3548a-302">Il existe deux listes de fichiers dans un fichier cab sur le CDN.</span><span class="sxs-lookup"><span data-stu-id="3548a-302">There are two file lists available in a cab file on the CDN.</span></span> <span data-ttu-id="3548a-303">1 répertorie les fichiers pour la version 32 bits d’Office et l’autre pour la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-303">One lists the files for the 32-bit version of Office and one for the 64-bit version of Office.</span></span> <span data-ttu-id="3548a-304">L’URL de l’emplacement de la liste des fichiers Office (OFL. Fichier CAB) est [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab).</span><span class="sxs-lookup"><span data-stu-id="3548a-304">The URL of the location of the Office File List (OFL.CAB) file is [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab).</span></span> <span data-ttu-id="3548a-305">Les listes de deux fichiers sont appelées :</span><span class="sxs-lookup"><span data-stu-id="3548a-305">The two file lists are called:</span></span>
  
- <span data-ttu-id="3548a-306">O365Client_32bit.Xml</span><span class="sxs-lookup"><span data-stu-id="3548a-306">O365Client_32bit.xml</span></span>
    
- <span data-ttu-id="3548a-307">O365Client_64bit.Xml</span><span class="sxs-lookup"><span data-stu-id="3548a-307">O365Client_64bit.xml</span></span>
    
<span data-ttu-id="3548a-308">Dans le code XML pour chaque fichier listes est un <UpdateFiles> nœud qui contient un attribut de version.</span><span class="sxs-lookup"><span data-stu-id="3548a-308">Within the XML for each of the file lists is an <UpdateFiles> node which contains a version attribute.</span></span>  <span data-ttu-id="3548a-309">`<UpdateFiles version="1.4">`.</span><span class="sxs-lookup"><span data-stu-id="3548a-309"></span></span> <span data-ttu-id="3548a-310">Cette version est incrémentée si des modifications sont apportées aux listes de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3548a-310">This version is incremented if changes are made to the file lists.</span></span>
  
<span data-ttu-id="3548a-311">Il existe deux paramètres qui doivent être combinés avec le code XML pour créer une image personnalisée :</span><span class="sxs-lookup"><span data-stu-id="3548a-311">There are two parameters that need to be combined with the XML to make a custom image:</span></span> 
  
- <span data-ttu-id="3548a-312">Remplacez la *version %* par le numéro de version d’Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-312">Replace  *%version%*  with the build version of Office.</span></span> <span data-ttu-id="3548a-313">Il peut être dérivé les métadonnées de mise à jour du Client (expliquée dans la section suivante).</span><span class="sxs-lookup"><span data-stu-id="3548a-313">This can be derived from the Client Update metadata (explained in the next section).</span></span> 
    
- <span data-ttu-id="3548a-314">Définir *baseURL* à l’aide de la valeur de l’URL associée à la branche qu'est créée pour l’image.</span><span class="sxs-lookup"><span data-stu-id="3548a-314">Define  *baseURL*  by using the URL value associated with the branch the image is being created for.</span></span> <span data-ttu-id="3548a-315">Il est dérivé les métadonnées de la mise à jour du Client, expliquée dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="3548a-315">This is derived from the Client Update metadata, explained in the following section.</span></span> 
    
<span data-ttu-id="3548a-316">Les étapes de création d’une image sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3548a-316">The steps for creating an image are:</span></span>
  
1. <span data-ttu-id="3548a-317">Ouvrez la liste des fichiers XML.</span><span class="sxs-lookup"><span data-stu-id="3548a-317">Open the XML file list.</span></span>
    
2. <span data-ttu-id="3548a-318">Remplacez les occurrences de *version %* avec la version Office applicable.</span><span class="sxs-lookup"><span data-stu-id="3548a-318">Replace occurrences of  *%version%*  with the applicable Office build version.</span></span> <span data-ttu-id="3548a-319">Le numéro de version peut être acquis à partir de releasehistory.xml comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="3548a-319">The build version can be acquired from releasehistory.xml as described later in this article.</span></span> 
    
3. <span data-ttu-id="3548a-320">Lire l’attribut URL de la branche cible.</span><span class="sxs-lookup"><span data-stu-id="3548a-320">Read the URL attribute for the target branch.</span></span>
    
4. <span data-ttu-id="3548a-321">Supprimer des nœuds de langue pour les langues non requis dans l’image personnalisée.</span><span class="sxs-lookup"><span data-stu-id="3548a-321">Remove language nodes for any languages not required in the custom image.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="3548a-322">Les nœuds de langage = « 0 » sont linguistiquement neutre et doit être inclus dans l’image.</span><span class="sxs-lookup"><span data-stu-id="3548a-322">Nodes with language='0' are language neutral and must be included in the image.</span></span> 
  
5. <span data-ttu-id="3548a-323">Construire une image locale du CDN par itération dans la liste des fichiers XML et la copie des fichiers CDN, lors de la création de la structure de dossiers selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="3548a-323">Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed.</span></span> 
    
   - <span data-ttu-id="3548a-324">Si l’attribut *rename* est fourni, puis se *Renommer* le fichier copié à la valeur fournie dans l’attribut renommer.</span><span class="sxs-lookup"><span data-stu-id="3548a-324">If the  *rename*  attribute is provided, then  *rename*  the copied file to the value provided in the rename attribute.</span></span> <span data-ttu-id="3548a-325">Cela permet de créer des fichiers v64.cab et v32.cab la valeur par défaut de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="3548a-325">This is used to create the top-level default v64.cab and v32.cab files.</span></span> <span data-ttu-id="3548a-326">Ces sont les versions du fichier cab plus haut niveau de build renommées et sont utilisés en tant que la version d’installation par défaut si la version n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3548a-326">These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified.</span></span> 
    
   - <span data-ttu-id="3548a-327">Utiliser des URL relativePath + nom de fichier pour construire l’emplacement CDN.</span><span class="sxs-lookup"><span data-stu-id="3548a-327">Use URL + relativePath + filename to construct the CDN location.</span></span>
    
<span data-ttu-id="3548a-328">Voici des exemples qui utilisent le canal mensuel (tel que défini par le `<baseURL>` nœud) et créer la version 16.0.4229.1004 à partir de releasehistory.xml.</span><span class="sxs-lookup"><span data-stu-id="3548a-328">The following are examples that use the Monthly channel (as defined by the  `<baseURL>` node) and build version 16.0.4229.1004 from releasehistory.xml.</span></span> 
  
```xml
<baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- <span data-ttu-id="3548a-329">Voici un fichier neutre linguistiques nécessaire pour toutes les langues.</span><span class="sxs-lookup"><span data-stu-id="3548a-329">The following is a language neutral file needed for all languages.</span></span> <span data-ttu-id="3548a-330">Le nom du fichier est v64_16.0.4229.1004.cab et il doit être copié à partir de `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` et renommé en `…/office/data/v64.cab`.</span><span class="sxs-lookup"><span data-stu-id="3548a-330">The name of the file is v64_16.0.4229.1004.cab and it should be copied from `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` and renamed to `…/office/data/v64.cab`.</span></span> 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- <span data-ttu-id="3548a-331">Ce qui suit est un fichier à inclure dans l’image en-US comme indiqué par le langage LCID = 1033.</span><span class="sxs-lookup"><span data-stu-id="3548a-331">The following is a file to be included in the en-US image as designated by the language LCID=1033.</span></span> <span data-ttu-id="3548a-332">Le nom du fichier est s641033.cab et il doit être copié à partir de `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` et pas renommé.</span><span class="sxs-lookup"><span data-stu-id="3548a-332">The name of the file is s641033.cab and it should be copied from `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` and not renamed.</span></span>
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="3548a-333">Vérification du hachage des fichiers .dat</span><span class="sxs-lookup"><span data-stu-id="3548a-333">Hash verification of .dat files</span></span>

<span data-ttu-id="3548a-334">Outils de création d’image peuvent vérifier l’intégrité des fichiers téléchargés .dat en comparant une valeur de hachage calculée avec la valeur de hachage fournie associée à chacun des fichiers .dat.</span><span class="sxs-lookup"><span data-stu-id="3548a-334">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files.</span></span> <span data-ttu-id="3548a-335">Voici un exemple d’un fichier .dat du canal avec 16.0.4229.1004 de version et langue à bulgare mensuel :</span><span class="sxs-lookup"><span data-stu-id="3548a-335">Following is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian:</span></span>
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- <span data-ttu-id="3548a-336">L’attribut **hashLocation** Spécifie l’emplacement de chemin d’accès relatif de le stream.x64.bg-bg.hash pour le fichier stream.x64.bg-bg.dat.</span><span class="sxs-lookup"><span data-stu-id="3548a-336">The **hashLocation** attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file.</span></span> <span data-ttu-id="3548a-337">Construire l’emplacement du fichier hachage en concaténant URL relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="3548a-337">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="3548a-338">Dans l’exemple suivant, l’emplacement de stream.x64.bg-bg.hash serait :</span><span class="sxs-lookup"><span data-stu-id="3548a-338">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="3548a-339">L’attribut **hashAlgo** indique quel algorithme de hachage utilisé.</span><span class="sxs-lookup"><span data-stu-id="3548a-339">The **hashAlgo** attribute specifies what hashing algorithm was used.</span></span> <span data-ttu-id="3548a-340">Dans ce cas Sha256 a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="3548a-340">In this case Sha256 was used.</span></span> 
    
  <span data-ttu-id="3548a-341">Pour valider l’intégrité du fichier stream.x64.bg-bg.dat, ouvrez le stream.x64.bg-bg.hash et lisez la valeur de hachage qui est la première ligne de texte dans le fichier de hachage.</span><span class="sxs-lookup"><span data-stu-id="3548a-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="3548a-342">Comparez cela à la valeur de hachage calculée (à l’aide de l’algorithme de hachage spécifié) pour vérifier l’intégrité du fichier téléchargé .dat.</span><span class="sxs-lookup"><span data-stu-id="3548a-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="3548a-343">L’exemple suivant montre le code c# pour lire la valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="3548a-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a><span data-ttu-id="3548a-344">Mises à jour du Client Office 365</span><span class="sxs-lookup"><span data-stu-id="3548a-344">Office 365 Client Updates</span></span>

<span data-ttu-id="3548a-345">Toutes les mises à jour Office 365 Client sont publiés dans le [Catalogue Microsoft Update](http://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="3548a-345">All Office 365 Client Updates are published to the [Microsoft Update Catalog](http://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="3548a-346">Mises à jour du Client Office 365 activer le logiciel de gestion traiter les mises à jour Office 365 Client d’une manière très similaire à n’importe quel autre WU mise à jour avec une exception ; les mises à jour client ne contiennent pas une charge réelle.</span><span class="sxs-lookup"><span data-stu-id="3548a-346">Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="3548a-347">Les mises à jour de Client Office 365 ne doivent pas être installé sur les clients mais plutôt utilisées pour déclencher le flux de travail avec le logiciel de gestion en remplaçant la commande d’installation avec COM en fonction de mécanisme d’installation ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="3548a-347">The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span> 
  
<span data-ttu-id="3548a-348">**La figure suivante illustre un diagramme du flux de travail de mise à jour du Client Office 365.**</span><span class="sxs-lookup"><span data-stu-id="3548a-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="3548a-349">![Diagramme de flux de travail pour les mises à jour du client O365PP.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagramme de flux de travail pour les mises à jour du client O365PP")</span><span class="sxs-lookup"><span data-stu-id="3548a-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="3548a-350">Chaque Office 365 mise à jour cliente qui est publiée inclut les métadonnées relatives à la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3548a-350">Each Office 365 Client Update that is published includes metadata about the update.</span></span> <span data-ttu-id="3548a-351">Ces métadonnées incluent un paramètre appelé *MoreInfoUrl* qui peut être utilisé pour obtenir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3548a-351">This metadata includes a parameter called  *MoreInfoUrl*  which can be used to derive the following information:</span></span> 
  
-  <span data-ttu-id="3548a-352">*Ver*: identifie la version d’Office associée à cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3548a-352">*Ver*: Identifies the Office version associated with this update.</span></span> 
    
-  <span data-ttu-id="3548a-353">*Branche*: identifie le canal de mise à jour pour cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3548a-353">*Branch*: Identifies the Update Channel for this update.</span></span> <span data-ttu-id="3548a-354">Les valeurs sont InsiderFast, initiés, tous les mois, cibles, requête large.</span><span class="sxs-lookup"><span data-stu-id="3548a-354">Values include InsiderFast, Insiders, Monthly, Targeted, Broad.</span></span> <span data-ttu-id="3548a-355">Valeurs supplémentaires peuvent être ajoutées à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="3548a-355">Additional values may be added in the future.</span></span> 
    
-  <span data-ttu-id="3548a-356">*Forme d’arc courbé*: identifie l’architecture de processeur associé à cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3548a-356">*Arch*: Identifies the processor architecture associated with this update.</span></span> 
    
-  <span data-ttu-id="3548a-357">*xmlVer*: la version des listes de fichiers XML qui doit être utilisé pour construire l’image de base pour cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3548a-357">*xmlVer*: The version of the XML file lists that should be used to construct the base image for this update.</span></span> 
    
-  <span data-ttu-id="3548a-358">*xmlPath*: chemin d’accès à la OFL. Répertorie les fichiers CAB qui contient le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="3548a-358">*xmlPath*: Path to the OFL.CAB file which contains the XML file lists.</span></span> 
    
-  <span data-ttu-id="3548a-359">*mlFile*: le nom de la liste des fichiers qui doit être utilisée pour cette mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3548a-359">*mlFile*: The name of the file list that should be used for this update.</span></span> <span data-ttu-id="3548a-360">La valeur sera O365Client_32bit ou O365Client_64bit et correspond à la forme d’arc courbé.</span><span class="sxs-lookup"><span data-stu-id="3548a-360">The value will be O365Client_32bit or O365Client_64bit and will match the Arch.</span></span> 
    
<span data-ttu-id="3548a-361">L’URL suivante est un exemple du paramètre *MoreInfoURL* qui fait référence pour les versions de mise à jour du client Office 365 pour la version 32 bits d’Office avec le numéro de version de 16.0.2342.2343 sur le canal en cours.</span><span class="sxs-lookup"><span data-stu-id="3548a-361">The following URL is an example of the  *MoreInfoURL*  parameter which refers to the Office 365 client update releases for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel.</span></span> 
  
<span data-ttu-id="3548a-362">http://officecdn.microsoft.com/pr/wsus/ofl.cabest l’emplacement des listes de fichiers XML pour cette mise à jour, spécifiquement le O365Client_32bit.xml à partir de la OFL. CAB.</span><span class="sxs-lookup"><span data-stu-id="3548a-362">http://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.</span></span>
  
[<span data-ttu-id="3548a-363">Versions de canal de mise à jour de client Office 365</span><span class="sxs-lookup"><span data-stu-id="3548a-363">Office 365 client update channel releases</span></span>](http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="3548a-364">Métadonnées supplémentaires pour l’automatisation de test de contenu</span><span class="sxs-lookup"><span data-stu-id="3548a-364">Additional metadata for automating content staging</span></span>

<span data-ttu-id="3548a-365">Outre les métadonnées qui sont publiée qui définit il sont également des fichiers XML publiés du CDN qui peuvent aider à fournir des informations supplémentaires sur les clients Office 365 qui sont disponibles à partir du CDN Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-365">In addition to the metadata that is published which defines there are also additional XML files published to the CDN that can help provide additional information about the Office 365 clients that are available from the Office CDN.</span></span>
  
<span data-ttu-id="3548a-366">**SKU. XML**</span><span class="sxs-lookup"><span data-stu-id="3548a-366">**SKUS.XML**</span></span>
  
<span data-ttu-id="3548a-367">Ce fichier XML est contenu dans un fichier CAB signé et publié du CDN Office à l’adresse suivante : [http://officecdn.microsoft.com/pr/wsus/skus.cab](http://officecdn.microsoft.com/pr/wsus/skus.cab).</span><span class="sxs-lookup"><span data-stu-id="3548a-367">This XML file is contained within a signed CAB and published to the Office CDN at the following URL: [http://officecdn.microsoft.com/pr/wsus/skus.cab](http://officecdn.microsoft.com/pr/wsus/skus.cab).</span></span>
  
<span data-ttu-id="3548a-368">Les métadonnées publiées dans ce fichier XML sont utile pour déterminer les produits qui sont disponibles pour le déploiement et de maintenance à partir du CDN Office ainsi que les différentes options pour chacun.</span><span class="sxs-lookup"><span data-stu-id="3548a-368">The metadata published in this XML file is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span> 
  
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

<span data-ttu-id="3548a-369">** \<ReleaseInfo\> ** nœud racine contient l’attribut PublishedDate qui identifie la date à laquelle ce fichier a été publié.</span><span class="sxs-lookup"><span data-stu-id="3548a-369">**\<ReleaseInfo\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="3548a-370">** \<SKU\> ** nœud identifie un référence SKU individuelle.</span><span class="sxs-lookup"><span data-stu-id="3548a-370">**\<SKU\>** node identifies an individual SKU.</span></span> 
  
- <span data-ttu-id="3548a-371">L’attribut *ProductID* identifie l’ID qui est passé en tant que l’attribut ID de la configuration.xml si vous utilisez l’outil de détection Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-371">The  *ProductID*  attribute identifies the ID that is passed as the ID attribute in the configuration.xml if using the ODT.</span></span> <span data-ttu-id="3548a-372">Par exemple, `<Product ID="O365ProPlusRetail">`.</span><span class="sxs-lookup"><span data-stu-id="3548a-372">For example, `<Product ID="O365ProPlusRetail">`.</span></span> 
    
- <span data-ttu-id="3548a-373">La *valeur par défaut* d’attributs, si la valeur True, identifie la référence SKU recommandé.</span><span class="sxs-lookup"><span data-stu-id="3548a-373">The  *Default*  attribute, if set to True, identifies the recommended SKU.</span></span> 
    
<span data-ttu-id="3548a-374">** \<Application\> ** nœuds sont utilisés pour définir les applications Office individuelles qui prend en charge par chaque version cliente.</span><span class="sxs-lookup"><span data-stu-id="3548a-374">**\<App\>** nodes are used to define the individual Office apps that each SKU supports.</span></span> 
  
- <span data-ttu-id="3548a-375">L’attribut *Name* est le nom d’application affiché.</span><span class="sxs-lookup"><span data-stu-id="3548a-375">The  *Name*  attribute is the displayed application name.</span></span> 
    
- <span data-ttu-id="3548a-376">L’attribut *AppID* est l’attribut ID passé le configuration.xml pour le ** \<ExcludeApp\> ** nœud si vous utilisez l’outil de détection Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-376">The  *AppID*  attribute is the ID attribute passed in the configuration.xml for the **\<ExcludeApp\>** node if using the ODT.</span></span> <span data-ttu-id="3548a-377">Par exemple, `<ExcludeApp ID="Publisher" />`.</span><span class="sxs-lookup"><span data-stu-id="3548a-377">For example, `<ExcludeApp ID="Publisher" />`.</span></span> 
    
<span data-ttu-id="3548a-378">**RELEASEHISTORY. XML**</span><span class="sxs-lookup"><span data-stu-id="3548a-378">**RELEASEHISTORY.XML**</span></span>
  
<span data-ttu-id="3548a-379">Ce fichier XML est contenu dans un fichier CAB signé et publié du CDN Office à l’emplacement suivant : [http://officecdn.microsoft.com/pr/wsus/releasehistory.cab](http://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span><span class="sxs-lookup"><span data-stu-id="3548a-379">This XML file is contained within a signed CAB and published to the Office CDN at the following location: [http://officecdn.microsoft.com/pr/wsus/releasehistory.cab](http://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span></span> 
  
<span data-ttu-id="3548a-380">Les métadonnées publiées dans ce fichier XML sont utile pour déterminer quels sont les canaux sont prises en charge pour la maintenance des mises à jour à partir du CDN Office ainsi que des informations sur l’historique de génération pour chacun des canaux pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3548a-380">The metadata published in this XML file is useful for determining which channels are supported for servicing updates from the Office CDN along with information about the build history for each of the supported channels.</span></span>
  
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

<span data-ttu-id="3548a-381">Le ** \<ReleaseHistory\> ** nœud racine contient l’attribut PublishedDate qui identifie la date à laquelle ce fichier a été publié.</span><span class="sxs-lookup"><span data-stu-id="3548a-381">The **\<ReleaseHistory\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="3548a-382">Le ** \<UpdateChannel\> ** nœud définit un canal pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3548a-382">The **\<UpdateChannel\>** node defines a supported channel.</span></span> 
  
- <span data-ttu-id="3548a-383">L’attribut *Name* définit l’ID du canal qui est utilisé pour passer à l’outil de détection Office dans le configuration.xml en tant que l’attribut de canal.</span><span class="sxs-lookup"><span data-stu-id="3548a-383">The  *Name*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="3548a-384">Exemple : `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span><span class="sxs-lookup"><span data-stu-id="3548a-384">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span></span> 
    
  > [!NOTE] 
  > <span data-ttu-id="3548a-385">Cet attribut est déconseillé et est utilisé pour la compatibilité descendante uniquement.</span><span class="sxs-lookup"><span data-stu-id="3548a-385">This attribute has been deprecated and is used for backward compatibility only.</span></span> <span data-ttu-id="3548a-386">Utilisez l’attribut ID à la place de l’attribut Name.</span><span class="sxs-lookup"><span data-stu-id="3548a-386">Use the ID attribute in place of the Name attribute.</span></span> 
    
- <span data-ttu-id="3548a-387">L’attribut *ID* définit l’ID du canal qui est utilisé pour passer à l’outil de détection Office dans le configuration.xml en tant que l’attribut de canal.</span><span class="sxs-lookup"><span data-stu-id="3548a-387">The  *ID*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="3548a-388">Exemple : `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span><span class="sxs-lookup"><span data-stu-id="3548a-388">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span></span> 
    
- <span data-ttu-id="3548a-389">L’attribut **DisplayName** est utilisé comme nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3548a-389">The **DisplayName**  attribute is used as the display name.</span></span> 
    
<span data-ttu-id="3548a-390">Le ** \<mettre à jour\> ** nœud permet de définir chaque mise à jour qui a été publié pour ce canal donné.</span><span class="sxs-lookup"><span data-stu-id="3548a-390">The **\<Update\>** node is used to define each update that has been published for that particular channel.</span></span> 
  
- <span data-ttu-id="3548a-391">Attribut la **plus récente** , si la valeur True, définit la mise à jour est la version la plus récente pour ce canal.</span><span class="sxs-lookup"><span data-stu-id="3548a-391">The **Latest**  attribute, if set to True, defines the release that is the latest release for that channel.</span></span> 
    
- <span data-ttu-id="3548a-392">L’attribut **Version** définit le numéro de version de cette mise à jour particulière.</span><span class="sxs-lookup"><span data-stu-id="3548a-392">The **Version** attribute defines the version number for this particular update.</span></span> 
    
- <span data-ttu-id="3548a-393">L’attribut **LegacyVersion** définit le numéro de version complète de cette mise à jour particulière.</span><span class="sxs-lookup"><span data-stu-id="3548a-393">The **LegacyVersion** attribute defines the full version number for this particular update.</span></span> 
    
- <span data-ttu-id="3548a-394">L’attribut **Build** définit le numéro de version de cette mise à jour particulière.</span><span class="sxs-lookup"><span data-stu-id="3548a-394">The **Build** attribute defines the build number for this particular update.</span></span> 
    
- <span data-ttu-id="3548a-395">L’attribut **PubTime** définit la date et l’heure à laquelle cette mise à jour a été publié sur le CDN Office.</span><span class="sxs-lookup"><span data-stu-id="3548a-395">The **PubTime** attribute defines the date and time at which this update was published to the Office CDN.</span></span> 
    

