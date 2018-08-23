---
title: Lien vers des fonctions MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5cb791d0d350a04864191a0a9d35a2f1c8b165d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577715"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="1287f-103">Lien vers des fonctions MAPI</span><span class="sxs-lookup"><span data-stu-id="1287f-103">Link to MAPI functions</span></span>

<span data-ttu-id="1287f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1287f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1287f-105">Il existe trois méthodes de liaison : la liaison implicite, liaison explicite et un nouveau modèle hybride à l’aide de la bibliothèque Stub MAPI.</span><span class="sxs-lookup"><span data-stu-id="1287f-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="1287f-106">Liaison implicite</span><span class="sxs-lookup"><span data-stu-id="1287f-106">Implicit linking</span></span>

<span data-ttu-id="1287f-107">Historiquement, l’appel de fonctions MAPI dans une application de messagerie toujours impliquée liaison à la bibliothèque Mapi32.lib.</span><span class="sxs-lookup"><span data-stu-id="1287f-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="1287f-108">Cette partie de routage des appels MAPI à la bibliothèque stub MAPI Windows, Mapi32.dll qui puis transférer les appels à l’implémentation du client MAPI par défaut en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1287f-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="1287f-109">Ce processus d’appel est appelé liaison implicite.</span><span class="sxs-lookup"><span data-stu-id="1287f-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="1287f-110">Le côté gauche de la figure suivante montre un exemple de liaison implicite utilisée dans un processus d’appel de fonction MAPI.</span><span class="sxs-lookup"><span data-stu-id="1287f-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="1287f-111">Le processus est initié par une application MAPI et implique la bibliothèque MAPI (Mapi32.lib) et le stub MAPI Windows (Mapi32.dll) et se termine par l’implémentation de client MAPI Outlook du stub MAPI (Msmapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="1287f-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="1287f-112">**Comparaison de liaison implicites et explicites.**</span><span class="sxs-lookup"><span data-stu-id="1287f-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="1287f-113">![Comparaison de liaison implicites et explicites] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparaison de liaison implicites et explicites")</span><span class="sxs-lookup"><span data-stu-id="1287f-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="1287f-114">Liaison explicite</span><span class="sxs-lookup"><span data-stu-id="1287f-114">Explicit linking</span></span>

<span data-ttu-id="1287f-115">Étant donné que le client MAPI par défaut prend en charge l’installation de la demande à l’aide de Windows Installer (MSI), vous pouvez développer des applications de messagerie directement sur le stub MAPI Outlook au lieu d’utiliser la bibliothèque MAPI et un stub MAPI Windows.</span><span class="sxs-lookup"><span data-stu-id="1287f-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="1287f-116">Le côté droit de la figure précédente montre un exemple d’un processus d’appel de fonction MAPI, commençant par une application MAPI, recherchez le chemin d’accès et le nom de la DLL pour le stub MAPI Outlook (étape 2 dans la section suivante) et l’émission d’appels de fonction dans la (stub MAPI Outlook étape 3 dans la section suivante).</span><span class="sxs-lookup"><span data-stu-id="1287f-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="1287f-117">La procédure suivante montre comment appeler des fonctions MAPI à l’aide de la liaison explicite.</span><span class="sxs-lookup"><span data-stu-id="1287f-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1287f-118">Ces informations sur la liaison explicite peuvent être superflues à vos besoins avec l’introduction de la MAPIStubLibrary.lib présenté dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="1287f-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="1287f-119">Comme le modèle implicite, la nouvelle bibliothèque gère tout et implémente la logique de liaison explicite qui charge d’Outlook MAPI directement.</span><span class="sxs-lookup"><span data-stu-id="1287f-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="1287f-120">Pour plus d’informations sur la liaison explicite, voir liaison explicitement.</span><span class="sxs-lookup"><span data-stu-id="1287f-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="1287f-121">Pour appeler les éléments de l’API MAPI sans la bibliothèque MAPI et le stub MAPI Windows</span><span class="sxs-lookup"><span data-stu-id="1287f-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="1287f-122">Dans votre fichier de programme, créez une liste globale des pointeurs fonction pour chaque élément MAPI API que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="1287f-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="1287f-123">L’exemple suivant montre cette étape.</span><span class="sxs-lookup"><span data-stu-id="1287f-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="1287f-124">Créez une fonction qui initialise les fonctions MAPI à lier à la DLL MAPI du client MAPI par défaut (par exemple, Msmapi32.dll de Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="1287f-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="1287f-125">Dans cette fonction, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1287f-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="1287f-126">Charger mapi32.dll à partir du répertoire système approprié.</span><span class="sxs-lookup"><span data-stu-id="1287f-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="1287f-127">x64 ou x86 en mode natif</span><span class="sxs-lookup"><span data-stu-id="1287f-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="1287f-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="1287f-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="1287f-129">x86 mode WoW</span><span class="sxs-lookup"><span data-stu-id="1287f-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="1287f-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="1287f-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="1287f-131">Appelez la fonction [FGetComponentPath](fgetcomponentpath.md) pour obtenir le chemin d’accès et le nom de la DLL qui implémente le sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="1287f-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="1287f-132">Pour plus d’informations, voir [Choisir une Version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="1287f-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="1287f-133">Charger la DLL en appelant la fonction LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="1287f-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="1287f-134">Initialiser le tableau de pointeur de fonction MAPI en appelant la fonction GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="1287f-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="1287f-135">L’exemple suivant montre les étapes précédentes :</span><span class="sxs-lookup"><span data-stu-id="1287f-135">The following example shows the previous steps:</span></span>
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. <span data-ttu-id="1287f-136">Enfin, appelez la fonction que vous avez créé à l’étape 2 dans votre application de messagerie avant d’effectuer des appels à des éléments de l’API de MAPI.</span><span class="sxs-lookup"><span data-stu-id="1287f-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="1287f-137">Vous devez annuler l’initialisation du sous-système MAPI avant la fermeture de votre application.</span><span class="sxs-lookup"><span data-stu-id="1287f-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="1287f-138">L’exemple suivant illustre cette étape :</span><span class="sxs-lookup"><span data-stu-id="1287f-138">The following example shows this step:</span></span> 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a><span data-ttu-id="1287f-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="1287f-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="1287f-140">L’arrivée de Microsoft Outlook 2010 et 64 bits MAPI, extension maintenant de Microsoft Outlook 2013, nécessite plus que l’API 32 bits traditionnel d’implémentation complète.</span><span class="sxs-lookup"><span data-stu-id="1287f-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="1287f-141">Un nouveau projet, la bibliothèque Stub MAPI, publié sur le site Web CodePlex fournit une solution de remplacement dans le désordre pour Mapi32.lib qui prend en charge la création d’applications MAPI 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1287f-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="1287f-142">MAPIStubLibrary.lib élimine le besoin pour une liaison explicite à MAPI, et ayant généré il, vous pouvez supprimer Mapi32.lib de vos paramètres de l’éditeur de liens, remplaçant par MAPIStubLibrary.lib ; aucune modification supplémentaire à votre code ne doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="1287f-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="1287f-143">Il supprime également la nécessité d’écrire du code **LoadLibrary**et **GetProcAddress** **FreeLibrary** pour gérer la plus récente exporte inclus dans ce fichier de bibliothèque mais pas dans Mapi32.lib, ce qui serait nécessaire si vous avez utilisé une liaison explicite.</span><span class="sxs-lookup"><span data-stu-id="1287f-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="1287f-144">Voici quelques-unes des nouvelles fonctions liées à partir de cette bibliothèque qui ne sont pas disponibles dans Mapi32.lib :</span><span class="sxs-lookup"><span data-stu-id="1287f-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="1287f-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="1287f-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="1287f-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="1287f-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="1287f-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="1287f-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="1287f-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="1287f-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="1287f-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="1287f-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="1287f-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="1287f-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="1287f-151">Une autre méthode de l’incorporation de la bibliothèque Stub MAPI consiste à copier les fichiers sources, MapiStubLibrary.cpp et StubUtils.cpp, directement dans votre projet et supprimer aucune liaison à Mapi32.lib ainsi que le code qui lie explicitement à MAPI.</span><span class="sxs-lookup"><span data-stu-id="1287f-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="1287f-152">Pour accéder aux fichiers de bibliothèque de Stub MAPI et pour plus d’informations sur la façon de créer et intégrer à votre projet, ainsi que des questions sur cette bibliothèque comme quand et pourquoi utiliser, voir la [Bibliothèque Stub de MAPI](http://mapistublibrary.codeplex.com/documentation) sur le site CodePlex.</span><span class="sxs-lookup"><span data-stu-id="1287f-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](http://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1287f-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1287f-153">See also</span></span>

- [<span data-ttu-id="1287f-154">Vue d'ensemble de la programmation MAPI</span><span class="sxs-lookup"><span data-stu-id="1287f-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="1287f-155">Installation du sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="1287f-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="1287f-156">Installer les fichiers d’en-tête MAPI</span><span class="sxs-lookup"><span data-stu-id="1287f-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="1287f-157">Choisir une version spécifique de MAPI à charger</span><span class="sxs-lookup"><span data-stu-id="1287f-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="1287f-158">Méthode de liaison à utiliser</span><span class="sxs-lookup"><span data-stu-id="1287f-158">Determining Which Linking Method to Use</span></span>](http://msdn.microsoft.com/en-us/library/253b8k2c.aspx)
- [<span data-ttu-id="1287f-159">Liaison d’un exécutable à une DLL</span><span class="sxs-lookup"><span data-stu-id="1287f-159">Linking an Executable to a DLL</span></span>](http://msdn.microsoft.com/en-us/library/9yd93633.aspx)
- [<span data-ttu-id="1287f-160">Configuration des clés MSI pour votre DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="1287f-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](http://msdn.microsoft.com/en-us/library/ee909494%28v=VS.85%29.aspx)

