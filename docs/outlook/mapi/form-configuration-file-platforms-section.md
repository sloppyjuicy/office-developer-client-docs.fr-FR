---
title: Section de formulaire Configuration de fichier [plateformes]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ddc6db2303d9d5f114fdb27b6e15e699a04e73f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783345"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="ec086-103">Section de formulaire Configuration de fichier [plateformes]</span><span class="sxs-lookup"><span data-stu-id="ec086-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="ec086-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec086-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec086-105">La section **[plateformes]** répertorie l’ensemble complet des plateformes prises en charge par ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="ec086-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="ec086-106">Chaque entrée de plateforme comprend le préfixe **plate-forme.**</span><span class="sxs-lookup"><span data-stu-id="ec086-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="ec086-107">_chaîne_dans laquelle la _chaîne_ est un code de chaîne arbitraire pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ec086-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="ec086-108">Chaque chaîne correspond à l’entrée de **l’UC** de des sections **[plateformes]** .</span><span class="sxs-lookup"><span data-stu-id="ec086-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="ec086-109">Chaque entrée dans la section **[plateformes]** définit une _chaîne de plateforme_ qui fait référence suivante **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="ec086-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="ec086-110">_chaîne de plateforme_ section **]** comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="ec086-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="ec086-111">La section **[plateformes]** répertorie l’ensemble complet des plateformes prises en charge par ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="ec086-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="ec086-112">Chaque entrée de plateforme comprend le préfixe **plate-forme.**</span><span class="sxs-lookup"><span data-stu-id="ec086-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="ec086-113">_chaîne_dans laquelle la _chaîne_ est un code de chaîne arbitraire pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ec086-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="ec086-114">Chaque chaîne correspond à l’entrée de **l’UC** de des sections **[plateformes]** .</span><span class="sxs-lookup"><span data-stu-id="ec086-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="ec086-115">Chaque entrée dans la section **[plateformes]** définit une _chaîne de plateforme_ qui fait référence suivante **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="ec086-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="ec086-116">_chaîne de plateforme_ section **]** comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="ec086-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="ec086-117">**[Plateformes]**</span><span class="sxs-lookup"><span data-stu-id="ec086-117">**[Platforms]**</span></span>
  
<span data-ttu-id="ec086-118">**Plateforme**.</span><span class="sxs-lookup"><span data-stu-id="ec086-118">**Platform**.</span></span> <span data-ttu-id="ec086-119">_chaîne_ =  _chaîne de plateforme_</span><span class="sxs-lookup"><span data-stu-id="ec086-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="ec086-120">Voici un exemple d’une section **[plateformes]** .</span><span class="sxs-lookup"><span data-stu-id="ec086-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="ec086-121">Chaque **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="ec086-121">Each **[Platform.**</span></span> <span data-ttu-id="ec086-122">_chaîne de plateforme_ section **]** contient deux entrées obligatoires, **l’UC** et **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="ec086-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="ec086-123">L’entrée de **l’UC** Spécifie le processeur et l’entrée **OSVersion** Spécifie le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ec086-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="ec086-124">Les valeurs de **processeur** valides sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ec086-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="ec086-125">**Entrée de l’UC**</span><span class="sxs-lookup"><span data-stu-id="ec086-125">**CPU Entry**</span></span>|<span data-ttu-id="ec086-126">**Processeur**</span><span class="sxs-lookup"><span data-stu-id="ec086-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec086-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="ec086-127">Ix86</span></span>  <br/> |<span data-ttu-id="ec086-128">Intel x 86 80 et processeurs Pentium, ainsi qu’équivalentes processeurs AMD, Cyrix, NextGen et autres fabricants.</span><span class="sxs-lookup"><span data-stu-id="ec086-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="ec086-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="ec086-129">MIPS</span></span>  <br/> |<span data-ttu-id="ec086-130">Processeurs MIPS R4000.</span><span class="sxs-lookup"><span data-stu-id="ec086-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="ec086-131">AXP</span><span class="sxs-lookup"><span data-stu-id="ec086-131">AXP</span></span>  <br/> |<span data-ttu-id="ec086-132">Processeur d’équipement Corporation Alpha AXP numériques.</span><span class="sxs-lookup"><span data-stu-id="ec086-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="ec086-133">PPC</span><span class="sxs-lookup"><span data-stu-id="ec086-133">PPC</span></span>  <br/> |<span data-ttu-id="ec086-134">Processeurs Motorola Power PC.</span><span class="sxs-lookup"><span data-stu-id="ec086-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="ec086-135">M68</span><span class="sxs-lookup"><span data-stu-id="ec086-135">M68</span></span>  <br/> |<span data-ttu-id="ec086-136">Processeurs Mororola 68 x 00.</span><span class="sxs-lookup"><span data-stu-id="ec086-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="ec086-137">Les valeurs valides **OSVersion** sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ec086-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="ec086-138">**Entrée OSVersion**</span><span class="sxs-lookup"><span data-stu-id="ec086-138">**OSVersion Entry**</span></span>|<span data-ttu-id="ec086-139">**Système d'exploitation**</span><span class="sxs-lookup"><span data-stu-id="ec086-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec086-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="ec086-140">Win3.1</span></span>  <br/> |<span data-ttu-id="ec086-141">Windows 3.1 et Windows pour les groupes de travail 3.11.</span><span class="sxs-lookup"><span data-stu-id="ec086-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="ec086-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="ec086-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="ec086-143">Windows NT 3.5 ou inférieure.</span><span class="sxs-lookup"><span data-stu-id="ec086-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="ec086-144">Windows 95</span><span class="sxs-lookup"><span data-stu-id="ec086-144">Win95</span></span>  <br/> |<span data-ttu-id="ec086-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="ec086-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="ec086-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="ec086-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="ec086-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="ec086-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="ec086-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="ec086-148">Mac7</span></span>  <br/> |<span data-ttu-id="ec086-149">Système Macintosh 7.</span><span class="sxs-lookup"><span data-stu-id="ec086-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="ec086-150">En outre, le **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="ec086-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="ec086-151">_chaîne de plateforme_ section **]** doit contenir un **fichier** ou un **liaisonavec** entrée.</span><span class="sxs-lookup"><span data-stu-id="ec086-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="ec086-152">L’entrée de **fichier** répertorie le formulaire serveur application fichier exécutable qui la bibliothèque de formulaires gère et charge dans un nouveau sous-répertoire dans le cache disque lorsque le formulaire est lancé.</span><span class="sxs-lookup"><span data-stu-id="ec086-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="ec086-153">Si une entrée **liaisonavec** est utilisée au lieu de cela, elle contient le nom d’une chaîne autre plate-forme d'où provient les informations du **fichier** .</span><span class="sxs-lookup"><span data-stu-id="ec086-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="ec086-154">Cela est utile si une version d’un formulaire prend en charge plusieurs plates-formes.</span><span class="sxs-lookup"><span data-stu-id="ec086-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="ec086-155">L’entrée de **Registre** est utilisée chaque fois que l’entrée de **fichier** est utilisée, il identifie la clé de Registre pour la bibliothèque de formulaires où se trouve le fichier exécutable de l’application de serveur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="ec086-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="ec086-156">Chaînes précédés d’une barre oblique inverse (\) sont placés à la racine du Registre.</span><span class="sxs-lookup"><span data-stu-id="ec086-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="ec086-157">Chaînes ne pas précédés d’une barre oblique inverse sont placés dans le _GUID_de HKEY_CLASSES_ROOT\CLSID\ \ clé de Registre, où _GUID_ est le **GUID** du formulaire.</span><span class="sxs-lookup"><span data-stu-id="ec086-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="ec086-158">Les caractères « %d » peuvent être utilisés pour indiquer le chemin d’accès du répertoire à partir de laquelle le fichier de configuration de formulaire a été lu.</span><span class="sxs-lookup"><span data-stu-id="ec086-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="ec086-159">Cela est utile pour spécifier d’autres fichiers avec les chemins d’accès par rapport au fichier de configuration de formulaire.</span><span class="sxs-lookup"><span data-stu-id="ec086-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="ec086-160">Entrées de **Registre** ou de **Plusieurs fichiers** peuvent être spécifiées à l’aide du fichier ou dans le Registre comme préfixe suivi par n’importe quel autre texte.</span><span class="sxs-lookup"><span data-stu-id="ec086-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="ec086-161">Le format de la **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="ec086-161">The format for the **[Platform.**</span></span> <span data-ttu-id="ec086-162">_chaîne de plateforme_ section **]** est :</span><span class="sxs-lookup"><span data-stu-id="ec086-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="ec086-163">**[Platform.**</span><span class="sxs-lookup"><span data-stu-id="ec086-163">**[Platform.**</span></span> <span data-ttu-id="ec086-164">_chaîne de plateforme_ **]**</span><span class="sxs-lookup"><span data-stu-id="ec086-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="ec086-165">**Processeur** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="ec086-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="ec086-166">**OSVersion** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="ec086-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="ec086-167">**Fichier** =  _chemin d’accès_</span><span class="sxs-lookup"><span data-stu-id="ec086-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="ec086-168">**Liaisonavec** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="ec086-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="ec086-169">**Registre** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="ec086-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="ec086-170">Voici deux exemples **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="ec086-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="ec086-171">_chaîne de plateforme_ sections **]** , à l’aide de l’entrée de **fichier** et un à l’aide de l’entrée **liaisonavec** .</span><span class="sxs-lookup"><span data-stu-id="ec086-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="ec086-172">Le **[plateforme.**</span><span class="sxs-lookup"><span data-stu-id="ec086-172">The **[Platform.**</span></span> <span data-ttu-id="ec086-173">_chaîne de plateforme_ section **]** est ignorée lorsque vous ajoutez un formulaire à la bibliothèque de formulaires local lorsqu’il est supposé que le programme d’installation a placé les fichiers constituant le Gestionnaire de classe de message dans le stockage local disponible en tant que nommé dans la section du gestionnaire dans le Registre OLE et effectué l’inscription OLE dans le Registre du système.</span><span class="sxs-lookup"><span data-stu-id="ec086-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

