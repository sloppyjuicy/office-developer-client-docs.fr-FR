---
title: Entrées de propriété dans les sections du service de message MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427996"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="717d4-103">Entrées de propriété dans les sections du service de message MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="717d4-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="717d4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="717d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="717d4-105">Les entrées qui définissent des propriétés utilisent ce format :</span><span class="sxs-lookup"><span data-stu-id="717d4-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="717d4-106">**balise de propriété** **=** valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="717d4-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="717d4-107">La balise de propriété peut être une balise de propriété MAPI standard si les données de configuration représentent l’une des propriétés prédéfinie par MAPI ou une balise non standard si les données ne représentent pas une propriété MAPI.</span><span class="sxs-lookup"><span data-stu-id="717d4-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="717d4-108">La balise nonstandard est réalisée en combinant la valeur d’un identificateur de propriété avec un type de propriété.</span><span class="sxs-lookup"><span data-stu-id="717d4-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="717d4-109">Le résultat est un nombre hexadécimal à 8 chiffres.</span><span class="sxs-lookup"><span data-stu-id="717d4-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="717d4-110">La valeur de la propriété peut être tout ce qui est logique pour la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="717d4-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="717d4-111">Les sections du service de message peuvent contenir une variété d’entrées selon le service de message configuré.</span><span class="sxs-lookup"><span data-stu-id="717d4-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="717d4-112">Les propriétés MAPI suivantes sont généralement incluses dans une section de services de message au format répertorié :</span><span class="sxs-lookup"><span data-stu-id="717d4-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="717d4-113">**PR_DISPLAY_NAME**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="717d4-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="717d4-114">**PR_SERVICE_DLL_NAME**  =   _nom du fichier DLL_</span><span class="sxs-lookup"><span data-stu-id="717d4-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="717d4-115">**PR_SERVICE_ENTRY_NAME**  =   _nom de la fonction de point d’entrée_</span><span class="sxs-lookup"><span data-stu-id="717d4-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="717d4-116">**PR_SERVICE_SUPPORT_FILES**  =   _liste des fichiers_</span><span class="sxs-lookup"><span data-stu-id="717d4-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="717d4-117">**PR_SERVICE_DELETE_FILES**  =   _liste des fichiers_</span><span class="sxs-lookup"><span data-stu-id="717d4-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="717d4-118">**PR_RESOURCE_FLAGS**  =   _masque de bits_</span><span class="sxs-lookup"><span data-stu-id="717d4-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="717d4-119">La **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) est le nom du service de message affiché dans l’interface utilisateur, le nom que l’utilisateur associe au service de message.</span><span class="sxs-lookup"><span data-stu-id="717d4-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="717d4-120">Le nom complet est une entrée facultative dans mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="717d4-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="717d4-121">Parfois, le nom complet est composé de deux parties . une partie affectée par le service de message et une partie affectée par l’utilisateur;</span><span class="sxs-lookup"><span data-stu-id="717d4-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="717d4-122">Si l’utilisateur est responsable de l’affectation de l’un des composants, cela est généralement géré avec une boîte de dialogue spéciale appelée feuille de propriétés fournie par le service de message sous le contrôle d’une application cliente.</span><span class="sxs-lookup"><span data-stu-id="717d4-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="717d4-123">Les informations fournies pour **l’entrée PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) sont le nom de la DLL qui contient le service de message.</span><span class="sxs-lookup"><span data-stu-id="717d4-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="717d4-124">Les informations fournies pour l’entrée **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) sont le nom de la fonction de point d’entrée dans cette DLL que MAPI appelle pour configurer le service de message.</span><span class="sxs-lookup"><span data-stu-id="717d4-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="717d4-125">Les fichiers répertoriés dans **l’entrée PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) sont des fichiers qui doivent être installés avec le service de message.</span><span class="sxs-lookup"><span data-stu-id="717d4-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="717d4-126">De même, les fichiers de **l’PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) doivent être supprimés lorsque le service de message est supprimé.</span><span class="sxs-lookup"><span data-stu-id="717d4-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="717d4-127">**L PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) est une collection d’options définies pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="717d4-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="717d4-128">Par exemple, le bit SERVICE_SINGLE_COPY est définie lorsque le service de message ne peut apparaître qu’une seule fois dans un profil donné.</span><span class="sxs-lookup"><span data-stu-id="717d4-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="717d4-129">Le bit SERVICE_NO_PRIMARY_IDENTITY est définie si le service de message ne fournit pas d’informations d’identité.</span><span class="sxs-lookup"><span data-stu-id="717d4-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="717d4-130">Deux exemples d’entrées de propriété non normes suivent.</span><span class="sxs-lookup"><span data-stu-id="717d4-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="717d4-131">La première entrée spécifie le chemin d’accès au fichier utilisé par le carnet d’adresses par défaut comme valeur de propriété ; la deuxième entrée spécifie une valeur de propriété numérique.</span><span class="sxs-lookup"><span data-stu-id="717d4-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="717d4-132">Les deux entrées ont une signification spécifique au service de message AB.</span><span class="sxs-lookup"><span data-stu-id="717d4-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


