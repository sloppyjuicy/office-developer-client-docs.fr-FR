---
title: Sélection d’une version spécifique de MAPI à charger
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344519"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="4cd31-103">Sélection d’une version spécifique de MAPI à charger</span><span class="sxs-lookup"><span data-stu-id="4cd31-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="4cd31-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cd31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cd31-105">Lorsque vous établissez une liaison explicite avec une implémentation de MAPI, vous devez soigneusement sélectionner l'implémentation à charger.</span><span class="sxs-lookup"><span data-stu-id="4cd31-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="4cd31-106">Il existe deux méthodes pour établir une liaison explicite avec une implémentation de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cd31-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="4cd31-107">Vous pouvez charger la bibliothèque de stub MAPI et spécifier dans le registre une DLL personnalisée pour charger et distribuer les appels MAPI à.</span><span class="sxs-lookup"><span data-stu-id="4cd31-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="4cd31-108">Vous pouvez implémenter l'algorithme de recherche de client MAPI pour rechercher la version de MAPI utilisée par le client de messagerie par défaut et le charger.</span><span class="sxs-lookup"><span data-stu-id="4cd31-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="4cd31-109">Étant donné que vous pouvez modifier les [paramètres du Registre stub Mapi32. dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) pour indiquer à votre application d'utiliser n'importe quelle implémentation de MAPI, nous vous recommandons de diriger votre application afin qu'elle utilise une implémentation de MAPI que vous avez testée avec.</span><span class="sxs-lookup"><span data-stu-id="4cd31-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="4cd31-110">Ce qui suit décrit les deux méthodes de liaison explicite.</span><span class="sxs-lookup"><span data-stu-id="4cd31-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="4cd31-111">Lecture à partir du Registre</span><span class="sxs-lookup"><span data-stu-id="4cd31-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="4cd31-112">Pour lire les informations d'implémentation MAPI à partir du Registre</span><span class="sxs-lookup"><span data-stu-id="4cd31-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="4cd31-113">Les clés de Registre qui indiquent une DLL personnalisée pour un client de messagerie se trouvent `HKLM\Software\Clients\Mail` sous la clé du client de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4cd31-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="4cd31-114">Le tableau suivant décrit ces clés:</span><span class="sxs-lookup"><span data-stu-id="4cd31-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="4cd31-115">**Clé**</span><span class="sxs-lookup"><span data-stu-id="4cd31-115">**Key**</span></span>|<span data-ttu-id="4cd31-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="4cd31-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="4cd31-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="4cd31-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="4cd31-118">Un ID de catégorie PublishComponent Windows Installer (GUID) qui identifie la DLL qui exporte les appels MAPI simples ou MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cd31-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="4cd31-119">Si cette clé est définie, elle est prioritaire sur la clé **DllPath** ou **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="4cd31-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="4cd31-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="4cd31-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="4cd31-121">Identificateur de paramètres régionaux (LCID) de votre application.</span><span class="sxs-lookup"><span data-stu-id="4cd31-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="4cd31-122">La première valeur de chaîne identifie une sous-clé `HKLM\Software` et les valeurs de chaîne suivantes identifient les valeurs de Registre sous cette clé qui contiennent des informations de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="4cd31-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="4cd31-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="4cd31-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="4cd31-124">LCID pour Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="4cd31-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="4cd31-125">La première valeur de chaîne identifie une sous-clé `HKLM\Software` et les valeurs de chaîne suivantes identifient les valeurs de Registre sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="4cd31-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="4cd31-126">Obtenez les informations de ces clés.</span><span class="sxs-lookup"><span data-stu-id="4cd31-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="4cd31-127">TransMettez les valeurs que vous avez obtenues de l'étape précédente à la fonction [FGetComponentPath](fgetcomponentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd31-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="4cd31-128">**FGetComponentPath** est une fonction qui est exportée par la bibliothèque de stub MAPI mapistub. dll.</span><span class="sxs-lookup"><span data-stu-id="4cd31-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="4cd31-129">Elle renvoie le chemin d'accès de la version personnalisée de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cd31-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="4cd31-130">Pour charger l'implémentation de MAPI marquée comme valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4cd31-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="4cd31-131">Lisez la `HKLM\Software\Clients\Mail::(default)` valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="4cd31-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="4cd31-132">Recherchez les informations pour le client indiqué comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="4cd31-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="4cd31-133">Notez que le client de messagerie par défaut ne peut pas implémenter MAPI étendu.</span><span class="sxs-lookup"><span data-stu-id="4cd31-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="4cd31-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="4cd31-134">Example</span></span>

<span data-ttu-id="4cd31-135">Pour charger MAPI tel qu'il est implémenté par Outlook, recherchez les clés `HKLM\Software\Clients\Mail\Microsoft Outlook` de Registre sous et transférez-les vers **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="4cd31-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="4cd31-136">**FGetComponentPath** renverra le chemin d'accès à l'implémentation d'Outlook de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cd31-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="4cd31-137">Si les clés **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID** ne sont pas définies, vérifiez la valeur de Registre **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="4cd31-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="4cd31-138">Si les clés sont définies, **FGetComponentPath** indique le chemin d'accès de l'implémentation MAPI du client.</span><span class="sxs-lookup"><span data-stu-id="4cd31-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="4cd31-139">Implémentation de l'algorithme de recherche de client MAPI</span><span class="sxs-lookup"><span data-stu-id="4cd31-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="4cd31-140">Le tableau suivant répertorie les quatre fonctions de MFCMAPI utilisées pour rechercher le chemin d'accès à une implémentation personnalisée de MAPI:</span><span class="sxs-lookup"><span data-stu-id="4cd31-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="4cd31-141">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="4cd31-141">**Function**</span></span>|<span data-ttu-id="4cd31-142">**Description**</span><span class="sxs-lookup"><span data-stu-id="4cd31-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="4cd31-143">Obtient le chemin d'accès de la bibliothèque MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cd31-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="4cd31-144">Obtient la clé de registre de messagerie MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cd31-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="4cd31-145">Obtient l'identificateur Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4cd31-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="4cd31-146">Obtient le chemin d'accès au composant à l'aide de [FGetComponentPath](fgetcomponentpath.md).</span><span class="sxs-lookup"><span data-stu-id="4cd31-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="4cd31-147">Étant donné que MFCMAPI charge l'implémentation par défaut de MAPI par défaut, si vous voulez utiliser une autre implémentation de MAPI, vous devez explicitement le lui indiquer.</span><span class="sxs-lookup"><span data-stu-id="4cd31-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="4cd31-148">Cette opération est effectuée à l'aide de la routine **MAPI Session\Load** .</span><span class="sxs-lookup"><span data-stu-id="4cd31-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="4cd31-149">Fonctionnement de ces fonctions</span><span class="sxs-lookup"><span data-stu-id="4cd31-149">How these functions work</span></span>

1. <span data-ttu-id="4cd31-150">Les appels `GetMAPIPath`MFCMAPI, en transMETTANT la valeur null pour le paramètre client, pour charger l'implémentation MAPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cd31-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="4cd31-151">`GetMAPIPath`appelle `GetMapiMsiIds` pour lire les valeurs de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="4cd31-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="4cd31-152">`GetMapiMsiIds`appels `GetMailKey` permettant d'ouvrir la clé de Registre pour le client de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cd31-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="4cd31-153">`GetMapiMsiIds`utilise le handle de Registre renvoyé `GetMailKey` par pour rechercher les valeurs de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="4cd31-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="4cd31-154">Les valeurs de **MSIComponentID**, **MSIApplicationLCID**et **MSIOfficeLCID**sont renvoyées à `GetMAPIPath`.</span><span class="sxs-lookup"><span data-stu-id="4cd31-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="4cd31-155">`GetMAPIPath`Ensuite, transmettez `GetComponentPath`-les à.</span><span class="sxs-lookup"><span data-stu-id="4cd31-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="4cd31-156">`GetComponentPath`charge la bibliothèque de stub MAPI, Mapi32. dll, à partir du répertoire système.</span><span class="sxs-lookup"><span data-stu-id="4cd31-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="4cd31-157">`GetComponentPath`récupère ensuite l'adresse de la fonction **FGetComponentPath** à partir de Mapi32. dll, en supposant que Mapi32. dll exporte **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="4cd31-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="4cd31-158">Si l'obtention de l'adresse de **FGetComponentPath** à partir de Mapi32 `GetComponentPath` . dll échoue, récupère l'adresse à partir de mapistub. dll.</span><span class="sxs-lookup"><span data-stu-id="4cd31-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="4cd31-159">`GetComponentPath`appelle ensuite **FGetComponentPath**, en obtenant le chemin d'accès de la version par défaut de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4cd31-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="4cd31-160">`GetMAPIPath`renvoie ensuite ce chemin d'accès à l'appelant, qui charge ensuite MAPI et y liens explicitement, comme décrit dans la rubrique [lien vers les fonctions MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4cd31-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="4cd31-161">Pour prendre en charge les copies localisées de MAPI pour l'anglais et les paramètres `GetMAPIPath` régionaux non anglais, lit les valeurs des sous-clés **MSIApplicationLCID** et **MSIOfficeLCID** .</span><span class="sxs-lookup"><span data-stu-id="4cd31-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="4cd31-162">`GetMAPIPath`appelle ensuite **FGetComponentPath**, en spécifiant d'abord **MSIApplicationLCID** en tant que **szQualifier**et en spécifiant de nouveau **MSIOfficeLCID** en tant que **szQualifier**.</span><span class="sxs-lookup"><span data-stu-id="4cd31-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="4cd31-163">Pour plus d'informations sur les clés de Registre pour les clients de messagerie qui prennent en charge les langues autres que l'anglais, consultez [la rubrique Setting up the MSI Keys for your MAPI dll](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4cd31-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="4cd31-164">Si MFCMAPI ne reçoit pas de chemin d'accès pour `GetMAPIPath`MAPI à l'aide de, il charge la bibliothèque de stubs MAPI à partir du répertoire système.</span><span class="sxs-lookup"><span data-stu-id="4cd31-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="4cd31-165">La valeur de Registre **MSMapiApps** abordée dans [mappage explicite des appels MAPI à des dll MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) s'applique uniquement lorsque la bibliothèque de stub MAPI est utilisée.</span><span class="sxs-lookup"><span data-stu-id="4cd31-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="4cd31-166">Les applications qui chargent une implémentation spécifique de MAPI ou chargent l'implémentation par défaut n'ont pas besoin de définir la clé de Registre **MSMapiApps** .</span><span class="sxs-lookup"><span data-stu-id="4cd31-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4cd31-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cd31-167">See also</span></span>

- [<span data-ttu-id="4cd31-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="4cd31-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="4cd31-169">Vue d’ensemble de la programmation MAPI</span><span class="sxs-lookup"><span data-stu-id="4cd31-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="4cd31-170">Lien vers les fonctions MAPI</span><span class="sxs-lookup"><span data-stu-id="4cd31-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="4cd31-171">Paramètres de Registre stub Mapi32. dll</span><span class="sxs-lookup"><span data-stu-id="4cd31-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="4cd31-172">Configuration des clés MSI pour votre DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="4cd31-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="4cd31-173">Mappage explicite des appels MAPI aux dll MAPI</span><span class="sxs-lookup"><span data-stu-id="4cd31-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

