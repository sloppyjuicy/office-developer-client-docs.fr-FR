---
title: Section Fichier de configuration de formulaire [Plateformes]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419127"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="f5494-103">Section Fichier de configuration de formulaire [Plateformes]</span><span class="sxs-lookup"><span data-stu-id="f5494-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="f5494-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5494-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5494-105">La section **[Plateformes]** répertorie l’ensemble complet des plateformes pris en charge par ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="f5494-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="f5494-106">Chaque entrée de plateforme se compose du **préfixe Platform.**</span><span class="sxs-lookup"><span data-stu-id="f5494-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="f5494-107">_,_ où  _chaîne est_ un code de chaîne arbitraire pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="f5494-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="f5494-108">Chaque chaîne correspond à l’entrée **processeur** d’une section **[Plateformes]** individuelle.</span><span class="sxs-lookup"><span data-stu-id="f5494-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="f5494-109">Chaque entrée d’une section **[Plateformes]** définit une chaîne de plateforme qui fait référence à une **autre [plateforme.** </span><span class="sxs-lookup"><span data-stu-id="f5494-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="f5494-110">_section chaîne de_ **plateforme ]** comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="f5494-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="f5494-111">La section **[Plateformes]** répertorie l’ensemble complet des plateformes pris en charge par ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="f5494-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="f5494-112">Chaque entrée de plateforme se compose du **préfixe Platform.**</span><span class="sxs-lookup"><span data-stu-id="f5494-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="f5494-113">_,_ où  _chaîne est_ un code de chaîne arbitraire pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="f5494-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="f5494-114">Chaque chaîne correspond à l’entrée **processeur** d’une section **[Plateformes]** individuelle.</span><span class="sxs-lookup"><span data-stu-id="f5494-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="f5494-115">Chaque entrée d’une section **[Plateformes]** définit une chaîne de plateforme qui fait référence à une **autre [plateforme.** </span><span class="sxs-lookup"><span data-stu-id="f5494-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="f5494-116">_section chaîne de_ **plateforme ]** comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="f5494-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="f5494-117">**[Plateformes]**</span><span class="sxs-lookup"><span data-stu-id="f5494-117">**[Platforms]**</span></span>
  
<span data-ttu-id="f5494-118">**Plateforme**.</span><span class="sxs-lookup"><span data-stu-id="f5494-118">**Platform**.</span></span> <span data-ttu-id="f5494-119">_string_  =   _chaîne de plateforme_</span><span class="sxs-lookup"><span data-stu-id="f5494-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="f5494-120">Voici un exemple de section **[Plateformes].**</span><span class="sxs-lookup"><span data-stu-id="f5494-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="f5494-121">Chaque **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="f5494-121">Each **[Platform.**</span></span> <span data-ttu-id="f5494-122">_section chaîne de_ **plateforme ]** contient les deux entrées requises, **processeur** et **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="f5494-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="f5494-123">**L’entrée du** processeur spécifie le processeur et l’entrée **OSVersion** spécifie le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f5494-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="f5494-124">Les valeurs **de** processeur valides sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f5494-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="f5494-125">**Entrée processeur**</span><span class="sxs-lookup"><span data-stu-id="f5494-125">**CPU Entry**</span></span>|<span data-ttu-id="f5494-126">**Processeur**</span><span class="sxs-lookup"><span data-stu-id="f5494-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5494-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="f5494-127">Ix86</span></span>  <br/> |<span data-ttu-id="f5494-128">Processeurs de série Intel 80x86 et Pentium, ainsi que des processeurs équivalents d’AMD, Cyrix, NextGen et d’autres fabricants.</span><span class="sxs-lookup"><span data-stu-id="f5494-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="f5494-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="f5494-129">MIPS</span></span>  <br/> |<span data-ttu-id="f5494-130">Processeurs de série MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="f5494-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="f5494-131">AXP</span><span class="sxs-lookup"><span data-stu-id="f5494-131">AXP</span></span>  <br/> |<span data-ttu-id="f5494-132">Processeur Alpha AXP Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="f5494-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="f5494-133">CPP</span><span class="sxs-lookup"><span data-stu-id="f5494-133">PPC</span></span>  <br/> |<span data-ttu-id="f5494-134">Processeurs de série Power PC.</span><span class="sxs-lookup"><span data-stu-id="f5494-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="f5494-135">M68</span><span class="sxs-lookup"><span data-stu-id="f5494-135">M68</span></span>  <br/> |<span data-ttu-id="f5494-136">Processeurs série 68 x 00.</span><span class="sxs-lookup"><span data-stu-id="f5494-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="f5494-137">Les valeurs **OSVersion** valides sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f5494-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="f5494-138">**Entrée OSVersion**</span><span class="sxs-lookup"><span data-stu-id="f5494-138">**OSVersion Entry**</span></span>|<span data-ttu-id="f5494-139">**Système d'exploitation**</span><span class="sxs-lookup"><span data-stu-id="f5494-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5494-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="f5494-140">Win3.1</span></span>  <br/> |<span data-ttu-id="f5494-141">Windows 3.1 et Windows for Workgroups 3.11.</span><span class="sxs-lookup"><span data-stu-id="f5494-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="f5494-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="f5494-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="f5494-143">Windows NT 3.5 ou inférieur.</span><span class="sxs-lookup"><span data-stu-id="f5494-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="f5494-144">Win95</span><span class="sxs-lookup"><span data-stu-id="f5494-144">Win95</span></span>  <br/> |<span data-ttu-id="f5494-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="f5494-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="f5494-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="f5494-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="f5494-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="f5494-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="f5494-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="f5494-148">Mac7</span></span>  <br/> |<span data-ttu-id="f5494-149">Système Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="f5494-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="f5494-150">En outre, la **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="f5494-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="f5494-151">_la_ section chaîne de plateforme **]** doit contenir une **entrée Fichier** ou **LinkTo.**</span><span class="sxs-lookup"><span data-stu-id="f5494-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="f5494-152">**L’entrée** Fichier répertorie le fichier exécutable de l’application serveur de formulaires que la bibliothèque de formulaires tient à jour et charge dans un nouveau sous-dossier dans le cache disque lors du lancement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f5494-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="f5494-153">Si une **entrée LinkTo** est utilisée à la place, elle contient le nom d’une chaîne de plateforme différente à partir de laquelle les informations **de** fichier sont prises.</span><span class="sxs-lookup"><span data-stu-id="f5494-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="f5494-154">Cela est utile si une version d’un formulaire prend en charge plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="f5494-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="f5494-155">**L’entrée** de Registre  est utilisée chaque fois que l’entrée de fichier est utilisée, elle identifie la clé de Registre de la bibliothèque de formulaires dans laquelle le fichier exécutable de l’application de serveur de formulaires est stocké.</span><span class="sxs-lookup"><span data-stu-id="f5494-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="f5494-156">Les chaînes précédées d’une barre oblique inverse ( \ ) sont placées à la racine du Registre.</span><span class="sxs-lookup"><span data-stu-id="f5494-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="f5494-157">Les chaînes non précédées d’une barre oblique inverse sont placées dans la HKEY_CLASSES_ROOT\CLSID\  _GUID_\ clé de Registre, où  _GUID_ est le **GUID** du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f5494-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="f5494-158">Les caractères « %d » peuvent être utilisés pour indiquer le chemin d’accès du répertoire à partir duquel le fichier de configuration du formulaire a été lu.</span><span class="sxs-lookup"><span data-stu-id="f5494-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="f5494-159">Cela est utile pour spécifier d’autres fichiers avec des noms de chemin d’accès relatifs au fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f5494-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="f5494-160">**Plusieurs entrées** de fichier ou de **Registre** peuvent être spécifiées en utilisant Fichier ou Registre comme préfixe suivi de tout autre texte.</span><span class="sxs-lookup"><span data-stu-id="f5494-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="f5494-161">Format de **la [plateforme.**</span><span class="sxs-lookup"><span data-stu-id="f5494-161">The format for the **[Platform.**</span></span> <span data-ttu-id="f5494-162">_la_ section chaîne **de plateforme ]** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f5494-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="f5494-163">**[Plateforme.**</span><span class="sxs-lookup"><span data-stu-id="f5494-163">**[Platform.**</span></span> <span data-ttu-id="f5494-164">_chaîne de plateforme_ **]**</span><span class="sxs-lookup"><span data-stu-id="f5494-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="f5494-165">**UC**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="f5494-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="f5494-166">**OSVersion**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="f5494-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="f5494-167">**Fichier**  =   _chemin d’accès_</span><span class="sxs-lookup"><span data-stu-id="f5494-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="f5494-168">**LinkTo**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="f5494-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="f5494-169">**Registre**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="f5494-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="f5494-170">Voici deux exemples **[Plateforme.**</span><span class="sxs-lookup"><span data-stu-id="f5494-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="f5494-171">_sections de chaîne_ de plateforme **]** : une à l’aide de **l’entrée Fichier** et une autre à l’entrée **LinkTo.**</span><span class="sxs-lookup"><span data-stu-id="f5494-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

<span data-ttu-id="f5494-172">**[Plateforme.**</span><span class="sxs-lookup"><span data-stu-id="f5494-172">The **[Platform.**</span></span> <span data-ttu-id="f5494-173"> la section chaîne de plateforme **]** est ignorée lors de l’ajout d’un formulaire à la bibliothèque de formulaires locale, lorsqu’il est supposé que le programme d’installation a placé les fichiers en charge du handler de classe de message dans le stockage local disponible, comme indiqué dans la section du responsable dans le Registre OLE, et a effectué l’inscription OLE dans le Registre du système.</span><span class="sxs-lookup"><span data-stu-id="f5494-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

