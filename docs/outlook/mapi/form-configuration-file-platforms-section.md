---
title: Section [plateformes] du fichier de configuration de formulaire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327509"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="4d964-103">Section [plateformes] du fichier de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="4d964-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="4d964-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d964-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d964-105">La section **[Platforms]** répertorie l'ensemble complet des plateformes prises en charge par ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d964-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="4d964-106">Chaque entrée de plateforme se compose de la plateforme de préfixe **.**</span><span class="sxs-lookup"><span data-stu-id="4d964-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="4d964-107">_String_, où _String_ est un code de chaîne arbitraire pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="4d964-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="4d964-108">Chaque chaîne correspond à l'entrée **processeur** d'une section **[Platforms]** individuelle.</span><span class="sxs-lookup"><span data-stu-id="4d964-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="4d964-109">Chaque entrée dans une section **[Platforms]** définit une _chaîne de plateforme_ qui fait référence à une nouvelle **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="4d964-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="4d964-110">_chaîne de plateforme_ **]** , comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4d964-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="4d964-111">La section **[Platforms]** répertorie l'ensemble complet des plateformes prises en charge par ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d964-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="4d964-112">Chaque entrée de plateforme se compose de la plateforme de préfixe **.**</span><span class="sxs-lookup"><span data-stu-id="4d964-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="4d964-113">_String_, où _String_ est un code de chaîne arbitraire pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="4d964-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="4d964-114">Chaque chaîne correspond à l'entrée **processeur** d'une section **[Platforms]** individuelle.</span><span class="sxs-lookup"><span data-stu-id="4d964-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="4d964-115">Chaque entrée dans une section **[Platforms]** définit une _chaîne de plateforme_ qui fait référence à une nouvelle **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="4d964-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="4d964-116">_chaîne de plateforme_ **]** , comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4d964-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="4d964-117">**Formes**</span><span class="sxs-lookup"><span data-stu-id="4d964-117">**[Platforms]**</span></span>
  
<span data-ttu-id="4d964-118">**Plateforme**.</span><span class="sxs-lookup"><span data-stu-id="4d964-118">**Platform**.</span></span> <span data-ttu-id="4d964-119">__ =  chaîne de_plateforme_ de chaîne</span><span class="sxs-lookup"><span data-stu-id="4d964-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="4d964-120">Voici un exemple de section **[Platforms]** .</span><span class="sxs-lookup"><span data-stu-id="4d964-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="4d964-121">Chaque **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="4d964-121">Each **[Platform.**</span></span> <span data-ttu-id="4d964-122">_chaîne de plateforme_ **]** contient les deux entrées requises, **CPU** et **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="4d964-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="4d964-123">L'entrée **CPU** spécifie le processeur et l'entrée **OSVersion** indique le système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="4d964-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="4d964-124">Les valeurs d' **UC** valides sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4d964-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="4d964-125">**Entrée de l'UC**</span><span class="sxs-lookup"><span data-stu-id="4d964-125">**CPU Entry**</span></span>|<span data-ttu-id="4d964-126">**Processeur**</span><span class="sxs-lookup"><span data-stu-id="4d964-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d964-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="4d964-127">Ix86</span></span>  <br/> |<span data-ttu-id="4d964-128">Processeurs Intel 80x86 et Pentium, ainsi que les processeurs équivalents de AMD, Cyrix, NextGen et d'autres fabricants.</span><span class="sxs-lookup"><span data-stu-id="4d964-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="4d964-129">MAUX</span><span class="sxs-lookup"><span data-stu-id="4d964-129">MIPS</span></span>  <br/> |<span data-ttu-id="4d964-130">Processeurs MIPS R4000 Series.</span><span class="sxs-lookup"><span data-stu-id="4d964-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="4d964-131">PLAT</span><span class="sxs-lookup"><span data-stu-id="4d964-131">AXP</span></span>  <br/> |<span data-ttu-id="4d964-132">Processeur Digital Equipment Corporation Alpha AXP.</span><span class="sxs-lookup"><span data-stu-id="4d964-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="4d964-133">CLIC</span><span class="sxs-lookup"><span data-stu-id="4d964-133">PPC</span></span>  <br/> |<span data-ttu-id="4d964-134">Processeurs Motorola Power PC Series.</span><span class="sxs-lookup"><span data-stu-id="4d964-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="4d964-135">M68</span><span class="sxs-lookup"><span data-stu-id="4d964-135">M68</span></span>  <br/> |<span data-ttu-id="4d964-136">Processeurs mororola série 68x00.</span><span class="sxs-lookup"><span data-stu-id="4d964-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="4d964-137">Les valeurs valides pour **OSVersion** sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4d964-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="4d964-138">**Entrée OSVersion**</span><span class="sxs-lookup"><span data-stu-id="4d964-138">**OSVersion Entry**</span></span>|<span data-ttu-id="4d964-139">**Système d'exploitation**</span><span class="sxs-lookup"><span data-stu-id="4d964-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d964-140">Win 3.1</span><span class="sxs-lookup"><span data-stu-id="4d964-140">Win3.1</span></span>  <br/> |<span data-ttu-id="4d964-141">Windows 3,1 et Windows pour Workgroups 3,11.</span><span class="sxs-lookup"><span data-stu-id="4d964-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="4d964-142">WinNT 3.5</span><span class="sxs-lookup"><span data-stu-id="4d964-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="4d964-143">Windows NT 3,5 ou inférieur.</span><span class="sxs-lookup"><span data-stu-id="4d964-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="4d964-144">95</span><span class="sxs-lookup"><span data-stu-id="4d964-144">Win95</span></span>  <br/> |<span data-ttu-id="4d964-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="4d964-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="4d964-146">WinNT 4.0</span><span class="sxs-lookup"><span data-stu-id="4d964-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="4d964-147">Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="4d964-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="4d964-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="4d964-148">Mac7</span></span>  <br/> |<span data-ttu-id="4d964-149">Macintosh système 7.</span><span class="sxs-lookup"><span data-stu-id="4d964-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="4d964-150">En outre, **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="4d964-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="4d964-151">_chaîne de plateforme_ **]** doit contenir un **fichier** ou une entrée **LinkTo** .</span><span class="sxs-lookup"><span data-stu-id="4d964-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="4d964-152">L'entrée de **fichier** répertorie le fichier exécutable de l'application serveur de formulaires que la bibliothèque de formulaires gère et charge dans un nouveau sous-répertoire du cache disque lors du lancement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d964-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="4d964-153">Si une entrée **LinkTo** est utilisée à la place, elle contient le nom d'une autre chaîne de plateforme à partir de laquelle les informations de **fichier** sont extraites.</span><span class="sxs-lookup"><span data-stu-id="4d964-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="4d964-154">Cette fonctionnalité est utile si une version d'un formulaire prend en charge plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="4d964-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="4d964-155">L'entrée de **Registre** est utilisée chaque fois que l'entrée de **fichier** est utilisée, elle identifie la clé de Registre pour la bibliothèque de formulaires dans laquelle le fichier exécutable de l'application form Server est stocké.</span><span class="sxs-lookup"><span data-stu-id="4d964-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="4d964-156">Les chaînes précédées d'une barre oblique inverse (\) sont placées à la racine du Registre.</span><span class="sxs-lookup"><span data-stu-id="4d964-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="4d964-157">Les chaînes qui ne sont pas précédées d'une barre oblique inverse sont placées dans la clé de Registre _GUID_HKEY_CLASSES_ROOT\CLSID\, où _GUID_ est le **GUID** du formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d964-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="4d964-158">Les caractères «% d» peuvent être utilisés pour indiquer le chemin d'accès du répertoire à partir duquel le fichier de configuration du formulaire a été lu.</span><span class="sxs-lookup"><span data-stu-id="4d964-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="4d964-159">Cela est utile pour spécifier d'autres fichiers avec des chemins d'accès relatifs au fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d964-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="4d964-160">**Plusieurs** entrées de fichier ou de **registre** peuvent être spécifiées à l'aide du fichier ou du registre en tant que préfixe suivi de tout autre texte.</span><span class="sxs-lookup"><span data-stu-id="4d964-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="4d964-161">Le format de la **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="4d964-161">The format for the **[Platform.**</span></span> <span data-ttu-id="4d964-162">_chaîne de plateforme_ **]** est la suivante:</span><span class="sxs-lookup"><span data-stu-id="4d964-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="4d964-163">**Plateforme.**</span><span class="sxs-lookup"><span data-stu-id="4d964-163">**[Platform.**</span></span> <span data-ttu-id="4d964-164">_chaîne de plateforme_ **]**</span><span class="sxs-lookup"><span data-stu-id="4d964-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="4d964-165">\*\*\*\* =  _Chaîne_ d'UC</span><span class="sxs-lookup"><span data-stu-id="4d964-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="4d964-166">\*\*\*\* =  _Chaîne_ OSVersion</span><span class="sxs-lookup"><span data-stu-id="4d964-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="4d964-167">\*\*\*\* =  _Chemin d'accès_ du fichier</span><span class="sxs-lookup"><span data-stu-id="4d964-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="4d964-168">\*\*\*\* =  _Chaîne_ LinkTo</span><span class="sxs-lookup"><span data-stu-id="4d964-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="4d964-169">\*\*\*\* =  _Chaîne_ de Registre</span><span class="sxs-lookup"><span data-stu-id="4d964-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="4d964-170">Voici deux exemples: **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="4d964-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="4d964-171">_chaîne de plateforme_ **]** , l'une à l'aide de l'entrée de **fichier** et l'autre à l'aide de l'entrée **LinkTo** .</span><span class="sxs-lookup"><span data-stu-id="4d964-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="4d964-172">**[Platform.**</span><span class="sxs-lookup"><span data-stu-id="4d964-172">The **[Platform.**</span></span> <span data-ttu-id="4d964-173">_chaîne de plateforme_ **]** est ignorée lors de l'ajout d'un formulaire à la bibliothèque de formulaires locale, lorsqu'il est supposé que le programme d'installation a placé les fichiers constituant le gestionnaire de classe de message dans un stockage local disponible tel que nommé dans la section du gestionnaire dans le registre OLE, et a effectué enregistrement OLE dans le Registre du système.</span><span class="sxs-lookup"><span data-stu-id="4d964-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

