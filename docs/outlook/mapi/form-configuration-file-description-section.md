---
title: Section [Description] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8ad5fd9cf437afc3999697792850548e4e5a1435
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582895"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="2320d-103">Section [Description] du fichier de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="2320d-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="2320d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2320d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2320d-105">La section **[Description]** répertorie toutes les propriétés du formulaire qui sont associées à des contrôles dans l’interface utilisateur du formulaire, ainsi que les attributs qui sont utilisés dans la localisation de l’écran.</span><span class="sxs-lookup"><span data-stu-id="2320d-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="2320d-106">Le **MessageClass**, **Clsid**et entrées **DisplayName** , permettant d’identifier le nom de classe de message du formulaire, son GUID et nom d’affichage de la classe de message, respectivement, sont des entrées obligatoires permet de rechercher le formulaire dans la bibliothèque de formulaires .</span><span class="sxs-lookup"><span data-stu-id="2320d-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="2320d-107">Les autres entrées sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="2320d-107">The remaining entries are optional.</span></span> <span data-ttu-id="2320d-108">Le format de la section **[Description]** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="2320d-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="2320d-109">La section **[Description]** répertorie toutes les propriétés du formulaire qui sont associées à des contrôles dans l’interface utilisateur du formulaire, ainsi que les attributs qui sont utilisés dans la localisation de l’écran.</span><span class="sxs-lookup"><span data-stu-id="2320d-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="2320d-110">Le **MessageClass**, **Clsid**et entrées **DisplayName** , permettant d’identifier le nom de classe de message du formulaire, son GUID et nom d’affichage de la classe de message, respectivement, sont des entrées obligatoires permet de rechercher le formulaire dans la bibliothèque de formulaires .</span><span class="sxs-lookup"><span data-stu-id="2320d-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="2320d-111">Les autres entrées sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="2320d-111">The remaining entries are optional.</span></span> <span data-ttu-id="2320d-112">Le format de la section **[Description]** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="2320d-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="2320d-113">**[Description] MessageClass** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="2320d-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="2320d-114">**CLSID** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="2320d-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="2320d-115">**DisplayName** =  _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="2320d-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="2320d-116">**SmallIcon** =  _chemin d’accès_</span><span class="sxs-lookup"><span data-stu-id="2320d-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="2320d-117">**LargeIcon** =  _chemin d’accès_</span><span class="sxs-lookup"><span data-stu-id="2320d-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="2320d-118">Entrées facultatives sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2320d-118">Optional entries are:</span></span>
  
 <span data-ttu-id="2320d-119">**Catégorie** =  _affiche la chaîne_</span><span class="sxs-lookup"><span data-stu-id="2320d-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="2320d-120">**Sous-catégorie** =  _affiche la chaîne_</span><span class="sxs-lookup"><span data-stu-id="2320d-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="2320d-121">**Commentaire** =  _affiche la chaîne_</span><span class="sxs-lookup"><span data-stu-id="2320d-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="2320d-122">**Propriétaire** =  _affiche la chaîne_</span><span class="sxs-lookup"><span data-stu-id="2320d-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="2320d-123">**Numéro de** =  _affiche la chaîne_</span><span class="sxs-lookup"><span data-stu-id="2320d-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="2320d-124">**Version** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="2320d-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="2320d-125">**Paramètres régionaux** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="2320d-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="2320d-126">**Masqué** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="2320d-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="2320d-127">**DesignerToolName** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="2320d-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="2320d-128">**DesignerToolGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="2320d-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="2320d-129">**DesignerRuntimeGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="2320d-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="2320d-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="2320d-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="2320d-131">**ComposeCommand** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="2320d-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="2320d-132">Les entrées de **catégorie** et une **sous-catégorie** sont utilisées par les programmes d’installation de l’écran pour configurer le classement par défaut des formulaires dans l’interface utilisateur de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="2320d-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="2320d-133">Par exemple, une hiérarchie peut être configurée où « Help Desk » est la catégorie et « Software » et « Hardware » ont été les sous-catégories.</span><span class="sxs-lookup"><span data-stu-id="2320d-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="2320d-134">Cette catégorisation puis utilisable par les applications de la visionneuse pour afficher les messages de manière plus organisée.</span><span class="sxs-lookup"><span data-stu-id="2320d-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="2320d-135">Les entrées de **commentaire**, le **propriétaire**et **nombre** sont toutes les chaînes de commentaire qui apparaissent dans l’interface utilisateur de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="2320d-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="2320d-136">Il s’agit des propriétés spécifiques du formulaire qui peuvent être utilisées à la discrétion du développeur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="2320d-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="2320d-137">Par exemple, l’entrée de **commentaire** peut être utilisée pour indiquer l’objectif de la forme, l’entrée de **propriétaire** est utilisée pour indiquer la personne ou l’organisation responsable de la maintenance du formulaire et le numéro utilisé pour effectuer le suivi de version différente du formulaire.</span><span class="sxs-lookup"><span data-stu-id="2320d-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="2320d-138">**Commentaire** entrée, jusqu'à 10 lignes de commentaires peut être incluse.</span><span class="sxs-lookup"><span data-stu-id="2320d-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="2320d-139">La première ligne de commentaires utilise le mot « Commentaire » comme clé, la deuxième ligne de commentaires utilise « Commentaires 1 » comme clé, et ainsi de suite par le biais de « Comment9 ».</span><span class="sxs-lookup"><span data-stu-id="2320d-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="2320d-140">Les entrées **LargeIcon** et **SmallIcon** sont utilisées pour spécifier le chemin d’accès pour les ressources de l’icône utilisée pour afficher les icônes dans l’interface utilisateur de l’application cliente, en règle générale, il s’agit des lignes de tableau qui incluent la **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou les colonnes de propriétés **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2320d-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="2320d-141">Noms de fichiers icône peuvent être spécifiés en tant que chemins d’accès relatif au répertoire où le fichier de configuration de formulaire est installé.</span><span class="sxs-lookup"><span data-stu-id="2320d-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="2320d-142">L’entrée de **Version** est utilisée pour indiquer le numéro de version du formulaire.</span><span class="sxs-lookup"><span data-stu-id="2320d-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="2320d-143">**Paramètres régionaux** est l’identificateur de langue de trois lettres de la bibliothèque de formulaires de destination.</span><span class="sxs-lookup"><span data-stu-id="2320d-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="2320d-144">Vous trouverez une liste des identificateurs suivants dans la _référence du programmeur Win32_.</span><span class="sxs-lookup"><span data-stu-id="2320d-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="2320d-145">L’entrée **masqué** indique si le formulaire doit être affiché dans l’interface utilisateur d’un fournisseur de bibliothèque de formulaires : 1 indique que le fichier est masqué et 0 indique que le formulaire est visible.</span><span class="sxs-lookup"><span data-stu-id="2320d-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="2320d-146">Un exemple de fichier de configuration de formulaire est affiché suivant.</span><span class="sxs-lookup"><span data-stu-id="2320d-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="2320d-147">L’entrée **ComposeInFolder** détermine si le formulaire est conçu pour être placé dans le dossier actif ou dans la boîte de réception de l’utilisateur lorsque l’utilisateur enregistre le message lors de sa composition : 1 indique que le formulaire doit être placé dans le dossier actif et 0 indique qu’il doit allez dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="2320d-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="2320d-148">L’entrée **ComposeCommand** est la chaîne doit être placée dans l’application cliente de composition de menu.</span><span class="sxs-lookup"><span data-stu-id="2320d-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="2320d-149">Si ce n’est pas spécifié, l’entrée **DisplayName** est utilisée.</span><span class="sxs-lookup"><span data-stu-id="2320d-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


