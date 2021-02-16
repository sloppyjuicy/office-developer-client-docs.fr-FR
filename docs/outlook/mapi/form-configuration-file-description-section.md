---
title: Section Fichier de configuration de formulaire [Description]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433093"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="ab9bc-103">Section Fichier de configuration de formulaire [Description]</span><span class="sxs-lookup"><span data-stu-id="ab9bc-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="ab9bc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab9bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab9bc-105">La section **[Description]** répertorie toutes les propriétés du formulaire associées aux contrôles dans l’interface utilisateur du formulaire, ainsi que les attributs utilisés pour localiser le formulaire.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="ab9bc-106">Les **entrées MessageClass,** **Clsid** et **DisplayName,** qui identifient respectivement le nom de la classe de message du formulaire, son GUID et le nom complet de la classe de message, sont des entrées requises pour localiser le formulaire dans la bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="ab9bc-107">Les entrées restantes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-107">The remaining entries are optional.</span></span> <span data-ttu-id="ab9bc-108">Le format de la section **[Description]** est le suivante :</span><span class="sxs-lookup"><span data-stu-id="ab9bc-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="ab9bc-109">La section **[Description]** répertorie toutes les propriétés du formulaire associées aux contrôles dans l’interface utilisateur du formulaire, ainsi que les attributs utilisés pour localiser le formulaire.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="ab9bc-110">Les **entrées MessageClass,** **Clsid** et **DisplayName,** qui identifient respectivement le nom de la classe de message du formulaire, son GUID et le nom complet de la classe de message, sont des entrées requises pour localiser le formulaire dans la bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="ab9bc-111">Les entrées restantes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-111">The remaining entries are optional.</span></span> <span data-ttu-id="ab9bc-112">Le format de la section **[Description]** est le suivante :</span><span class="sxs-lookup"><span data-stu-id="ab9bc-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="ab9bc-113">**[Description] MessageClass**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="ab9bc-114">**Clsid**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="ab9bc-115">**DisplayName**  =   _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="ab9bc-116">**SmallIcon**  =   _chemin d’accès_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="ab9bc-117">**LargeIcon**  =   _chemin d’accès_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="ab9bc-118">Les entrées facultatives sont :</span><span class="sxs-lookup"><span data-stu-id="ab9bc-118">Optional entries are:</span></span>
  
 <span data-ttu-id="ab9bc-119">**Catégorie**  =   _chaîne affichée_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="ab9bc-120">**Sous-catégorie**  =   _chaîne affichée_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="ab9bc-121">**Commentaire**  =   _chaîne affichée_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="ab9bc-122">**Propriétaire**  =   _chaîne affichée_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="ab9bc-123">**Number**  =   _chaîne affichée_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="ab9bc-124">**Version**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="ab9bc-125">**Paramètres régionaux**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="ab9bc-126">**Hidden**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="ab9bc-127">**DesignerToolName**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="ab9bc-128">**DesignerToolGuid**  =   _clsid_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="ab9bc-129">**DesignerRuntimeGuid**  =   _clsid_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="ab9bc-130">**ComposeInFolder**  =   _0|1_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="ab9bc-131">**ComposeCommand**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="ab9bc-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="ab9bc-132">Les **entrées** **Catégorie** et Sous-catégorie sont utilisées par les programme d’installation de formulaires pour configurer la catégorisation par défaut des formulaires dans l’interface utilisateur de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="ab9bc-133">Par exemple, une hiérarchie peut être définie où « Help Desk » est la catégorie et « Software » et « Hardware » sont les sous-catégories.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="ab9bc-134">Cette catégorisation peut ensuite être utilisée par les applications de visionneuse pour afficher les messages de manière plus organisée.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="ab9bc-135">Les **entrées Comment**, **Propriétaire** et **Nombre** sont toutes des chaînes de commentaires qui apparaissent dans l’interface utilisateur de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="ab9bc-136">Ce sont des propriétés spécifiques au formulaire qui peuvent être utilisées à la discrétion du développeur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="ab9bc-137">Par exemple,  l’entrée Commentaire peut être utilisée pour  indiquer l’objectif du formulaire, l’entrée Propriétaire utilisée pour indiquer la personne ou l’organisation responsable de la maintenance du formulaire et le numéro utilisé pour suivre la version différente du formulaire.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="ab9bc-138">Pour **l’entrée** Commentaire, vous pouvez inclure jusqu’à dix lignes de commentaires.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="ab9bc-139">La première ligne de commentaires utilise le mot « Comment » comme clé, la deuxième ligne utilise « Comment1 » comme clé, et ainsi de suite par le biais de « Comment9 ».</span><span class="sxs-lookup"><span data-stu-id="ab9bc-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="ab9bc-140">Les entrées **LargeIcon** et **SmallIcon** sont utilisées pour spécifier le chemin d’accès aux ressources d’icône utilisées pour afficher les icônes dans l’interface utilisateur de l’application cliente, généralement pour les lignes de tableau qui incluent les colonnes de propriété **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ab9bc-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="ab9bc-141">Les noms de fichier d’icône peuvent être spécifiés en tant que chemins d’accès par rapport au répertoire où le fichier de configuration du formulaire est installé.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="ab9bc-142">**L’entrée** Version est utilisée pour indiquer le numéro de version du formulaire.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="ab9bc-143">**Locale est** l’identificateur de langue à trois lettres de la bibliothèque de formulaires de destination.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="ab9bc-144">Vous pouvez trouver la liste de ces identificateurs dans la Référence du _programmeur Win32._</span><span class="sxs-lookup"><span data-stu-id="ab9bc-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="ab9bc-145">**L’entrée** Masquée indique si le formulaire doit être affiché dans l’interface utilisateur d’un fournisseur de bibliothèque de formulaires : 1 indique que le fichier est masqué et 0 indique que le formulaire est visible.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="ab9bc-146">Voici un exemple de fichier de configuration de formulaire.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="ab9bc-147">L’entrée **ComposeInFolder** contrôle si le formulaire est conçu pour être placé dans le dossier actuel ou dans la boîte de réception de l’utilisateur lorsque l’utilisateur enregistre le message lors de sa composition : 1 indique que le formulaire doit être placé dans le dossier actuel et 0 indique qu’il doit être placé dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="ab9bc-148">**L’entrée ComposeCommand** est la chaîne à placer dans le menu composition de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="ab9bc-149">Si ce n’est pas spécifié, **l’entrée DisplayName** est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ab9bc-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


