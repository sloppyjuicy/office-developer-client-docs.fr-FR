---
title: Choisissez une version spécifique de MAPI à charger
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399731"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="f48b3-103">Choisissez une version spécifique de MAPI à charger</span><span class="sxs-lookup"><span data-stu-id="f48b3-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="f48b3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f48b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f48b3-105">Lors de la liaison explicite à une implémentation de MAPI, vous devez sélectionner avec soin l’implémentation à charger.</span><span class="sxs-lookup"><span data-stu-id="f48b3-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="f48b3-106">Il existe deux méthodes pour lier explicitement à une implémentation de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f48b3-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="f48b3-107">Vous pouvez charger la bibliothèque stub MAPI et spécifier dans le Registre des appels vers une DLL personnalisée pour charger et distribuer MAPI.</span><span class="sxs-lookup"><span data-stu-id="f48b3-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="f48b3-108">Vous pouvez implémenter l’algorithme de recherche MAPI client pour rechercher la version de MAPI utilisé par le client de messagerie par défaut et le charger.</span><span class="sxs-lookup"><span data-stu-id="f48b3-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="f48b3-109">Étant donné que vous pouvez modifier les [Paramètres de Registre Stub Mapi32.dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) pour diriger votre application pour utiliser une implémentation de MAPI, nous vous recommandons de rediriger votre application pour utiliser une implémentation de MAPI que vous avez testé avec.</span><span class="sxs-lookup"><span data-stu-id="f48b3-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="f48b3-110">La liste suivante décrit les deux méthodes de liaison explicite.</span><span class="sxs-lookup"><span data-stu-id="f48b3-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="f48b3-111">Lecture à partir du Registre</span><span class="sxs-lookup"><span data-stu-id="f48b3-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="f48b3-112">Pour lire les informations de mise en œuvre de MAPI à partir du Registre</span><span class="sxs-lookup"><span data-stu-id="f48b3-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="f48b3-113">Les clés de Registre qui indiquent une DLL personnalisée pour un client de messagerie sont situés sous le `HKLM\Software\Clients\Mail` clés du client de messagerie.</span><span class="sxs-lookup"><span data-stu-id="f48b3-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="f48b3-114">Le tableau suivant décrit ces clés :</span><span class="sxs-lookup"><span data-stu-id="f48b3-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="f48b3-115">**Clé**</span><span class="sxs-lookup"><span data-stu-id="f48b3-115">**Key**</span></span>|<span data-ttu-id="f48b3-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="f48b3-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="f48b3-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="f48b3-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="f48b3-118">Une catégorie de Windows Installer PublishComponent ID (GUID) qui identifie la DLL qui exporte simple MAPI ou MAPI appelle.</span><span class="sxs-lookup"><span data-stu-id="f48b3-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="f48b3-119">Si définie, cette clé est prioritaire sur la touche **DLLPath** ou **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="f48b3-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="f48b3-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="f48b3-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="f48b3-121">Identificateur de paramètres régionaux (LCID) pour votre application.</span><span class="sxs-lookup"><span data-stu-id="f48b3-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="f48b3-122">La première chaîne de valeur identifie une sous-clé à partir de `HKLM\Software` et valeurs de chaîne suivantes identifient les valeurs de Registre qui contiennent des informations de paramètres régionaux sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="f48b3-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="f48b3-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="f48b3-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="f48b3-124">LCID pour Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f48b3-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="f48b3-125">La première chaîne de valeur identifie une sous-clé à partir de `HKLM\Software` et valeurs de chaîne suivantes identifient les valeurs sous cette clé de Registre.</span><span class="sxs-lookup"><span data-stu-id="f48b3-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="f48b3-126">Obtenir les informations à partir de ces clés.</span><span class="sxs-lookup"><span data-stu-id="f48b3-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="f48b3-127">Transmettre les valeurs que vous avez obtenu à partir de l’étape précédente à la fonction [FGetComponentPath](fgetcomponentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="f48b3-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="f48b3-128">**FGetComponentPath** est une fonction qui est exportée par la bibliothèque de stub MAPI Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="f48b3-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="f48b3-129">Elle renvoie le chemin d’accès de la version personnalisée de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f48b3-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="f48b3-130">Pour charger l’implémentation de MAPI marqué comme valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f48b3-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="f48b3-131">Lire la `HKLM\Software\Clients\Mail::(default)` valeur de Registre.</span><span class="sxs-lookup"><span data-stu-id="f48b3-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="f48b3-132">Rechercher des informations pour le client indiqué comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="f48b3-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f48b3-133">Notez que le client de messagerie par défaut ne peut pas implémenter interface MAPI étendue.</span><span class="sxs-lookup"><span data-stu-id="f48b3-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="f48b3-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="f48b3-134">Example</span></span>

<span data-ttu-id="f48b3-135">Pour charger MAPI telle qu’implémentée par Outlook, rechercher les clés de Registre sous `HKLM\Software\Clients\Mail\Microsoft Outlook` et transmettez-les à **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="f48b3-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="f48b3-136">**FGetComponentPath** renvoie le chemin d’accès pour l’implémentation d’Outlook de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f48b3-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="f48b3-137">Si les clés de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID** ne sont pas définies, vérifiez la valeur de Registre **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="f48b3-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="f48b3-138">Si les clés sont définies, **FGetComponentPath** donne le chemin d’accès de l’implémentation du client de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f48b3-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="f48b3-139">L’implémentation de l’algorithme de recherche de clients MAPI</span><span class="sxs-lookup"><span data-stu-id="f48b3-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="f48b3-140">Le tableau suivant répertorie les quatre fonctions de MFCMAPI qui sont utilisées pour rechercher le chemin d’accès d’une implémentation personnalisée de MAPI :</span><span class="sxs-lookup"><span data-stu-id="f48b3-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="f48b3-141">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f48b3-141">**Function**</span></span>|<span data-ttu-id="f48b3-142">**Description**</span><span class="sxs-lookup"><span data-stu-id="f48b3-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="f48b3-143">Obtient le chemin d’accès de la bibliothèque MAPI.</span><span class="sxs-lookup"><span data-stu-id="f48b3-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="f48b3-144">Obtient la clé de Registre de messagerie MAPI.</span><span class="sxs-lookup"><span data-stu-id="f48b3-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="f48b3-145">Obtient l’identificateur de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f48b3-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="f48b3-146">Obtient le chemin d’accès du composant à l’aide de [FGetComponentPath](fgetcomponentpath.md).</span><span class="sxs-lookup"><span data-stu-id="f48b3-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="f48b3-147">Car MFCMAPI charge l’implémentation par défaut de MAPI par défaut, si vous souhaitez utiliser une autre implémentation de MAPI, vous devez explicitement lui à le faire.</span><span class="sxs-lookup"><span data-stu-id="f48b3-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="f48b3-148">Cette opération est effectuée à l’aide de la routine **Session\Load MAPI** .</span><span class="sxs-lookup"><span data-stu-id="f48b3-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="f48b3-149">Fonctionnement de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="f48b3-149">How these functions work</span></span>

1. <span data-ttu-id="f48b3-150">Appels MFCMAPI `GetMAPIPath`, passant NULL pour le paramètre client, pour charger l’implémentation de MAPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="f48b3-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="f48b3-151">`GetMAPIPath`appels `GetMapiMsiIds` pour lire les valeurs pour **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="f48b3-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="f48b3-152">`GetMapiMsiIds`appels `GetMailKey` pour ouvrir la clé de Registre pour le client de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="f48b3-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="f48b3-153">`GetMapiMsiIds`utilise le handle de Registre retourné par `GetMailKey` pour rechercher des valeurs pour **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="f48b3-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="f48b3-154">Les valeurs de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**, sont renvoyés à `GetMAPIPath`.</span><span class="sxs-lookup"><span data-stu-id="f48b3-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="f48b3-155">`GetMAPIPath`transmet à `GetComponentPath`.</span><span class="sxs-lookup"><span data-stu-id="f48b3-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="f48b3-156">`GetComponentPath`charge la bibliothèque stub MAPI, Mapi32.dll, à partir du répertoire du système.</span><span class="sxs-lookup"><span data-stu-id="f48b3-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="f48b3-157">`GetComponentPath`puis extrait l’adresse de la fonction **FGetComponentPath** Mapi32.dll, en supposant que Mapi32.dll exporte **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="f48b3-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="f48b3-158">Si l’obtention de l’adresse de **FGetComponentPath** à partir de Mapi32.dll échoue, `GetComponentPath` récupère l’adresse Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="f48b3-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="f48b3-159">`GetComponentPath`appelle ensuite **FGetComponentPath**, obtenir le chemin d’accès de la version par défaut de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f48b3-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="f48b3-160">`GetMAPIPath`renvoie ensuite ce chemin d’accès à l’appelant, puis charge MAPI et lie explicitement lui comme décrit dans [le lien fonctions MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f48b3-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="f48b3-161">Pour prendre en charge les copies localisées de MAPI pour l’anglais et les paramètres régionaux non anglais, `GetMAPIPath` lit les valeurs pour les sous-clés **MSIApplicationLCID** et **MSIOfficeLCID** .</span><span class="sxs-lookup"><span data-stu-id="f48b3-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="f48b3-162">`GetMAPIPath`appelle ensuite **FGetComponentPath**, tout d’abord spécifiant **MSIApplicationLCID** sous **szQualifier**, puis à nouveau spécifiant **MSIOfficeLCID** comme **szQualifier**.</span><span class="sxs-lookup"><span data-stu-id="f48b3-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="f48b3-163">Pour plus d’informations sur les clés de Registre pour les clients de messagerie qui prennent en charge des langues, voir [Paramètre Up the MSI clés pour votre DLL MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f48b3-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="f48b3-164">Si MFCMAPI ne reçoit pas d’un chemin d’accès pour l’utilisation de MAPI `GetMAPIPath`, il charge la bibliothèque de stub MAPI à partir du répertoire du système.</span><span class="sxs-lookup"><span data-stu-id="f48b3-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="f48b3-165">La valeur de Registre **MSMapiApps** présentée dans le [Mappage explicitement des appels MAPI aux DLL MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) s’applique uniquement lorsque la bibliothèque Stub MAPI est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f48b3-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="f48b3-166">Applications qui chargement une implémentation de MAPI ou chargement l’implémentation par défaut n’ont pas définir la clé de Registre **MSMapiApps** .</span><span class="sxs-lookup"><span data-stu-id="f48b3-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f48b3-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f48b3-167">See also</span></span>

- [<span data-ttu-id="f48b3-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="f48b3-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="f48b3-169">Vue d'ensemble de la programmation MAPI</span><span class="sxs-lookup"><span data-stu-id="f48b3-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="f48b3-170">Lien vers les fonctions MAPI</span><span class="sxs-lookup"><span data-stu-id="f48b3-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="f48b3-171">Paramètres de Registre Stub Mapi32.dll</span><span class="sxs-lookup"><span data-stu-id="f48b3-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="f48b3-172">Configuration des clés MSI pour votre DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="f48b3-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="f48b3-173">Mappage explicitement des appels MAPI aux DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="f48b3-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

