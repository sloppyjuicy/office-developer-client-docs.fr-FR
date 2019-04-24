---
title: Section [Description] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320985"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="44dd4-103">Section [Description] du fichier de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="44dd4-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="44dd4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44dd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44dd4-105">La section **[Description]** répertorie toutes les propriétés du formulaire qui sont associées aux contrôles dans l'interface utilisateur du formulaire, ainsi que les attributs utilisés lors de la recherche du formulaire.</span><span class="sxs-lookup"><span data-stu-id="44dd4-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="44dd4-106">Les entrées **MessageClass**, **CLSID**et **DisplayName** , qui identifient le nom de la classe de message, son GUID et le nom d'affichage de la classe de message, respectivement, sont des entrées requises pour localiser le formulaire dans la bibliothèque de formulaires. .</span><span class="sxs-lookup"><span data-stu-id="44dd4-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="44dd4-107">Les entrées restantes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="44dd4-107">The remaining entries are optional.</span></span> <span data-ttu-id="44dd4-108">Le format de la section **[Description]** est le suivant:</span><span class="sxs-lookup"><span data-stu-id="44dd4-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="44dd4-109">La section **[Description]** répertorie toutes les propriétés du formulaire qui sont associées aux contrôles dans l'interface utilisateur du formulaire, ainsi que les attributs utilisés lors de la recherche du formulaire.</span><span class="sxs-lookup"><span data-stu-id="44dd4-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="44dd4-110">Les entrées **MessageClass**, **CLSID**et **DisplayName** , qui identifient le nom de la classe de message, son GUID et le nom d'affichage de la classe de message, respectivement, sont des entrées requises pour localiser le formulaire dans la bibliothèque de formulaires. .</span><span class="sxs-lookup"><span data-stu-id="44dd4-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="44dd4-111">Les entrées restantes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="44dd4-111">The remaining entries are optional.</span></span> <span data-ttu-id="44dd4-112">Le format de la section **[Description]** est le suivant:</span><span class="sxs-lookup"><span data-stu-id="44dd4-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="44dd4-113">\*\*Description \*\* =  _Chaîne_ MessageClass</span><span class="sxs-lookup"><span data-stu-id="44dd4-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="44dd4-114">\*\*\*\* =  _GUID_ CLSID</span><span class="sxs-lookup"><span data-stu-id="44dd4-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="44dd4-115">**DisplayName** =  _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="44dd4-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="44dd4-116">\*\*\*\* =  _Chemin d'accès_ SmallIcon</span><span class="sxs-lookup"><span data-stu-id="44dd4-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="44dd4-117">\*\*\*\* =  _Chemin d'accès_ LargeIcon</span><span class="sxs-lookup"><span data-stu-id="44dd4-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="44dd4-118">Les entrées facultatives sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="44dd4-118">Optional entries are:</span></span>
  
 <span data-ttu-id="44dd4-119">\*\*\*\* =  _Chaîne affichée_ sous la catégorie</span><span class="sxs-lookup"><span data-stu-id="44dd4-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="44dd4-120">\*\*\*\* =  _Chaîne affichée sous_ -catégorie</span><span class="sxs-lookup"><span data-stu-id="44dd4-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="44dd4-121">\*\*\*\* =  _Chaîne affichée_ de commentaire</span><span class="sxs-lookup"><span data-stu-id="44dd4-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="44dd4-122">\*\*\*\* =  _Chaîne affichée_ par le propriétaire</span><span class="sxs-lookup"><span data-stu-id="44dd4-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="44dd4-123">\*\*\*\* =  _Chaîne affichée_ en nombre</span><span class="sxs-lookup"><span data-stu-id="44dd4-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="44dd4-124">\*\*\*\* =  _Entier_ de version</span><span class="sxs-lookup"><span data-stu-id="44dd4-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="44dd4-125">**Chaîne de paramètres régionaux**__  =  </span><span class="sxs-lookup"><span data-stu-id="44dd4-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="44dd4-126">\*\*\*\* =  _Entier_ masqué</span><span class="sxs-lookup"><span data-stu-id="44dd4-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="44dd4-127">\*\*\*\* =  _Chaîne_ DesignerToolName</span><span class="sxs-lookup"><span data-stu-id="44dd4-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="44dd4-128">\*\*\*\* =  _CLSID_ DesignerToolGuid</span><span class="sxs-lookup"><span data-stu-id="44dd4-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="44dd4-129">\*\*\*\* =  _CLSID_ DesignerRuntimeGuid</span><span class="sxs-lookup"><span data-stu-id="44dd4-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="44dd4-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="44dd4-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="44dd4-131">\*\*\*\* =  _Chaîne_ ComposeCommand</span><span class="sxs-lookup"><span data-stu-id="44dd4-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="44dd4-132">Les entrées de **catégorie** et de **sous-catégorie** sont utilisées par les programmes d'installation de formulaire pour configurer la catégorisation par défaut des formulaires dans l'interface utilisateur de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="44dd4-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="44dd4-133">Par exemple, une hiérarchie peut être configurée où «support technique» est la catégorie et «logiciel» et «matériel» étaient les sous-catégories.</span><span class="sxs-lookup"><span data-stu-id="44dd4-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="44dd4-134">Cette catégorisation peut ensuite être utilisée par les applications de la visionneuse pour afficher les messages d'une manière plus organisée.</span><span class="sxs-lookup"><span data-stu-id="44dd4-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="44dd4-135">Les entrées de **Commentaire**, de **propriétaire**et de **numéro** sont toutes des chaînes de commentaires qui apparaissent dans l'interface utilisateur de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="44dd4-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="44dd4-136">Il s'agit de propriétés spécifiques qui peuvent être utilisées à la discrétion du développeur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="44dd4-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="44dd4-137">Par exemple, l'entrée de **Commentaire** peut être utilisée pour indiquer l'objectif du formulaire, l'entrée de **propriétaire** utilisée pour indiquer la personne ou l'organisation chargée de la gestion du formulaire, ainsi que le numéro utilisé pour suivre différentes versions du formulaire.</span><span class="sxs-lookup"><span data-stu-id="44dd4-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="44dd4-138">Pour l'entrée de **Commentaire** , jusqu'à dix lignes de commentaires peuvent être incluses.</span><span class="sxs-lookup"><span data-stu-id="44dd4-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="44dd4-139">La première ligne de commentaires utilise le mot «commentaire» comme clé, la deuxième ligne de commentaires utilise «Comment1» comme clé, et ainsi de suite par «Comment9».</span><span class="sxs-lookup"><span data-stu-id="44dd4-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="44dd4-140">Les entrées **LargeIcon** et **SmallIcon** sont utilisées pour spécifier le chemin d'accès aux ressources d'icône utilisées pour afficher les icônes dans l'interface utilisateur de l'application cliente, en règle générale, il s'agit des lignes de tableau qui incluent le **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)). ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="44dd4-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="44dd4-141">Les noms de fichiers d'icônes peuvent être spécifiés sous forme de chemins d'accès par rapport au répertoire dans lequel le fichier de configuration du formulaire est installé.</span><span class="sxs-lookup"><span data-stu-id="44dd4-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="44dd4-142">L'entrée de **version** est utilisée pour indiquer le numéro de version du formulaire.</span><span class="sxs-lookup"><span data-stu-id="44dd4-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="44dd4-143">**Paramètres régionaux** est l'identificateur de langue à trois lettres de la bibliothèque de formulaires de destination.</span><span class="sxs-lookup"><span data-stu-id="44dd4-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="44dd4-144">Une liste de ces identificateurs est disponible dans le _Guide de référence du programmeUr Win32_.</span><span class="sxs-lookup"><span data-stu-id="44dd4-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="44dd4-145">L' \*\*\*\* entrée masquée indique si le formulaire doit être affiché dans l'interface utilisateur d'un fournisseur de bibliothèque de formulaires: 1 indique que le fichier est masqué et 0 indique que le formulaire est visible.</span><span class="sxs-lookup"><span data-stu-id="44dd4-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="44dd4-146">Un exemple de fichier de configuration de formulaire est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="44dd4-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="44dd4-147">L'entrée **ComposeInFolder** contrôle si le formulaire est conçu pour être placé dans le dossier actif ou dans la boîte de réception de l'utilisateur lorsque l'utilisateur enregistre le message pendant qu'il le compose: 1 indique que le formulaire doit se trouver dans le dossier actif et 0 indique qu'il doit Accédez à la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="44dd4-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="44dd4-148">L'entrée **ComposeCommand** est la chaîne à placer dans le menu de composition de l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="44dd4-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="44dd4-149">Si ce n'est pas spécifié, l'entrée **DisplayName** est utilisée.</span><span class="sxs-lookup"><span data-stu-id="44dd4-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


