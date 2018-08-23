---
title: Section [Plates-formes] du fichier de configuration de formulaire
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d86edfb6fcc72c5968a8ff5d9cd739e20e5dec43
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589895"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="af821-103">Section [Plates-formes] du fichier de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="af821-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="af821-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af821-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af821-105">La section **[plateformes]** répertorie l’ensemble complet des plateformes prises en charge par ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="af821-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="af821-106">Chaque entrée de plateforme comprend le préfixe **plate-forme.**</span><span class="sxs-lookup"><span data-stu-id="af821-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="af821-107">_chaîne_dans laquelle la _chaîne_ est un code de chaîne arbitraire pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="af821-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="af821-108">Chaque chaîne correspond à l’entrée de **l’UC** de des sections **[plateformes]** .</span><span class="sxs-lookup"><span data-stu-id="af821-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="af821-109">Chaque entrée dans la section **[plateformes]** définit une _chaîne de plateforme_ qui fait référence suivante **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="af821-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="af821-110">_chaîne de plateforme_ section **]** comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="af821-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="af821-111">La section **[plateformes]** répertorie l’ensemble complet des plateformes prises en charge par ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="af821-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="af821-112">Chaque entrée de plateforme comprend le préfixe **plate-forme.**</span><span class="sxs-lookup"><span data-stu-id="af821-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="af821-113">_chaîne_dans laquelle la _chaîne_ est un code de chaîne arbitraire pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="af821-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="af821-114">Chaque chaîne correspond à l’entrée de **l’UC** de des sections **[plateformes]** .</span><span class="sxs-lookup"><span data-stu-id="af821-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="af821-115">Chaque entrée dans la section **[plateformes]** définit une _chaîne de plateforme_ qui fait référence suivante **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="af821-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="af821-116">_chaîne de plateforme_ section **]** comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="af821-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="af821-117">**[Plateformes]**</span><span class="sxs-lookup"><span data-stu-id="af821-117">**[Platforms]**</span></span>
  
<span data-ttu-id="af821-118">**Plateforme**.</span><span class="sxs-lookup"><span data-stu-id="af821-118">**Platform**.</span></span> <span data-ttu-id="af821-119">_chaîne_ =  _chaîne de plateforme_</span><span class="sxs-lookup"><span data-stu-id="af821-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="af821-120">Voici un exemple d’une section **[plateformes]** .</span><span class="sxs-lookup"><span data-stu-id="af821-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="af821-121">Chaque **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="af821-121">Each **[Platform.**</span></span> <span data-ttu-id="af821-122">_chaîne de plateforme_ section **]** contient deux entrées obligatoires, **l’UC** et **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="af821-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="af821-123">L’entrée de **l’UC** Spécifie le processeur et l’entrée **OSVersion** Spécifie le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="af821-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="af821-124">Les valeurs de **processeur** valides sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="af821-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="af821-125">**Entrée de l’UC**</span><span class="sxs-lookup"><span data-stu-id="af821-125">**CPU Entry**</span></span>|<span data-ttu-id="af821-126">**Processeur**</span><span class="sxs-lookup"><span data-stu-id="af821-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af821-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="af821-127">Ix86</span></span>  <br/> |<span data-ttu-id="af821-128">Intel x 86 80 et processeurs Pentium, ainsi qu’équivalentes processeurs AMD, Cyrix, NextGen et autres fabricants.</span><span class="sxs-lookup"><span data-stu-id="af821-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="af821-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="af821-129">MIPS</span></span>  <br/> |<span data-ttu-id="af821-130">Processeurs MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="af821-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="af821-131">AXP</span><span class="sxs-lookup"><span data-stu-id="af821-131">AXP</span></span>  <br/> |<span data-ttu-id="af821-132">Processeur d’équipement Corporation Alpha AXP numériques.</span><span class="sxs-lookup"><span data-stu-id="af821-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="af821-133">PPC</span><span class="sxs-lookup"><span data-stu-id="af821-133">PPC</span></span>  <br/> |<span data-ttu-id="af821-134">Processeurs Motorola Power PC.</span><span class="sxs-lookup"><span data-stu-id="af821-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="af821-135">M68</span><span class="sxs-lookup"><span data-stu-id="af821-135">M68</span></span>  <br/> |<span data-ttu-id="af821-136">Processeurs Mororola 68 x 00.</span><span class="sxs-lookup"><span data-stu-id="af821-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="af821-137">Les valeurs valides **OSVersion** sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="af821-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="af821-138">**Entrée OSVersion**</span><span class="sxs-lookup"><span data-stu-id="af821-138">**OSVersion Entry**</span></span>|<span data-ttu-id="af821-139">**Système d'exploitation**</span><span class="sxs-lookup"><span data-stu-id="af821-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af821-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="af821-140">Win3.1</span></span>  <br/> |<span data-ttu-id="af821-141">Windows 3.1 et Windows pour les groupes de travail 3.11.</span><span class="sxs-lookup"><span data-stu-id="af821-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="af821-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="af821-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="af821-143">Windows NT 3.5 ou inférieure.</span><span class="sxs-lookup"><span data-stu-id="af821-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="af821-144">Windows 95</span><span class="sxs-lookup"><span data-stu-id="af821-144">Win95</span></span>  <br/> |<span data-ttu-id="af821-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="af821-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="af821-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="af821-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="af821-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="af821-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="af821-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="af821-148">Mac7</span></span>  <br/> |<span data-ttu-id="af821-149">Système Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="af821-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="af821-150">En outre, le **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="af821-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="af821-151">_chaîne de plateforme_ section **]** doit contenir un **fichier** ou un **liaisonavec** entrée.</span><span class="sxs-lookup"><span data-stu-id="af821-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="af821-152">L’entrée de **fichier** répertorie le formulaire serveur application fichier exécutable qui la bibliothèque de formulaires gère et charge dans un nouveau sous-répertoire dans le cache disque lorsque le formulaire est lancé.</span><span class="sxs-lookup"><span data-stu-id="af821-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="af821-153">Si une entrée **liaisonavec** est utilisée au lieu de cela, elle contient le nom d’une chaîne autre plate-forme d'où provient les informations du **fichier** .</span><span class="sxs-lookup"><span data-stu-id="af821-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="af821-154">Cela est utile si une version d’un formulaire prend en charge plusieurs plates-formes.</span><span class="sxs-lookup"><span data-stu-id="af821-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="af821-155">L’entrée de **Registre** est utilisée chaque fois que l’entrée de **fichier** est utilisée, il identifie la clé de Registre pour la bibliothèque de formulaires où se trouve le fichier exécutable de l’application de serveur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="af821-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="af821-156">Chaînes précédés d’une barre oblique inverse (\) sont placés à la racine du Registre.</span><span class="sxs-lookup"><span data-stu-id="af821-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="af821-157">Chaînes ne pas précédés d’une barre oblique inverse sont placés dans le _GUID_de HKEY_CLASSES_ROOT\CLSID\ \ clé de Registre, où _GUID_ est le **GUID** du formulaire.</span><span class="sxs-lookup"><span data-stu-id="af821-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="af821-158">Les caractères « %d » peuvent être utilisés pour indiquer le chemin d’accès du répertoire à partir de laquelle le fichier de configuration de formulaire a été lu.</span><span class="sxs-lookup"><span data-stu-id="af821-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="af821-159">Cela est utile pour spécifier d’autres fichiers avec les chemins d’accès par rapport au fichier de configuration de formulaire.</span><span class="sxs-lookup"><span data-stu-id="af821-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="af821-160">Entrées de **Registre** ou de **Plusieurs fichiers** peuvent être spécifiées à l’aide du fichier ou dans le Registre comme préfixe suivi par n’importe quel autre texte.</span><span class="sxs-lookup"><span data-stu-id="af821-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="af821-161">Le format de la **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="af821-161">The format for the **[Platform.**</span></span> <span data-ttu-id="af821-162">_chaîne de plateforme_ section **]** est :</span><span class="sxs-lookup"><span data-stu-id="af821-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="af821-163">**[Platform.**</span><span class="sxs-lookup"><span data-stu-id="af821-163">**[Platform.**</span></span> <span data-ttu-id="af821-164">_chaîne de plateforme_ **]**</span><span class="sxs-lookup"><span data-stu-id="af821-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="af821-165">**Processeur** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="af821-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="af821-166">**OSVersion** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="af821-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="af821-167">**Fichier** =  _chemin d’accès_</span><span class="sxs-lookup"><span data-stu-id="af821-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="af821-168">**Liaisonavec** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="af821-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="af821-169">**Registre** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="af821-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="af821-170">Voici deux exemples **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="af821-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="af821-171">_chaîne de plateforme_ sections **]** , à l’aide de l’entrée de **fichier** et un à l’aide de l’entrée **liaisonavec** .</span><span class="sxs-lookup"><span data-stu-id="af821-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="af821-172">Le **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="af821-172">The **[Platform.**</span></span> <span data-ttu-id="af821-173">_chaîne de plateforme_ section **]** est ignorée lorsque vous ajoutez un formulaire à la bibliothèque de formulaires local lorsqu’il est supposé que le programme d’installation a placé les fichiers constituant le Gestionnaire de classe de message dans le stockage local disponible en tant que nommé dans la section du gestionnaire dans le Registre OLE et effectué l’inscription OLE dans le Registre du système.</span><span class="sxs-lookup"><span data-stu-id="af821-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

