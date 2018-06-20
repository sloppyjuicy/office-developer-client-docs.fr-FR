---
title: Section de formulaire Configuration de fichier [verbes]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5fe1b064b48bc9112a872677fbf5042b7dfe5449
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783343"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="38d21-103">Section de formulaire Configuration de fichier [verbes]</span><span class="sxs-lookup"><span data-stu-id="38d21-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="38d21-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38d21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38d21-105">La section **[verbes]** répertorie l’ensemble complet des verbes pris en charge par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="38d21-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="38d21-106">Le format de la section **[verbes]** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="38d21-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="38d21-107">**[Verbes]**</span><span class="sxs-lookup"><span data-stu-id="38d21-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="38d21-108">**Verb1** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="38d21-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="38d21-109">Voici un exemple d’une section **[verbes]** .</span><span class="sxs-lookup"><span data-stu-id="38d21-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="38d21-110">Chaque verbe est défini dans un distinct **[verbe.**</span><span class="sxs-lookup"><span data-stu-id="38d21-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="38d21-111">_chaîne_ section **]** .</span><span class="sxs-lookup"><span data-stu-id="38d21-111">_string_ **]** section.</span></span> <span data-ttu-id="38d21-112">A **[verbe.**</span><span class="sxs-lookup"><span data-stu-id="38d21-112">A **[Verb.**</span></span> <span data-ttu-id="38d21-113">_chaîne_ section **]** décrit un verbe unique offert par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="38d21-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="38d21-114">L’entrée **DisplayName** dans un **[verbe.**</span><span class="sxs-lookup"><span data-stu-id="38d21-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="38d21-115">_chaîne_ section **]** Spécifie le nom de la commande affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38d21-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="38d21-116">L’entrée de **Code** correspond au numéro de verbe passé dans la méthode [IMAPIForm::DoVerb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="38d21-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="38d21-117">La syntaxe de la **[verbe.**</span><span class="sxs-lookup"><span data-stu-id="38d21-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="38d21-118">_chaîne_ section **]** est :</span><span class="sxs-lookup"><span data-stu-id="38d21-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="38d21-119">**[Verbe.**</span><span class="sxs-lookup"><span data-stu-id="38d21-119">**[Verb.**</span></span> <span data-ttu-id="38d21-120">_chaîne_ **]**</span><span class="sxs-lookup"><span data-stu-id="38d21-120">_string_ **]**</span></span>
  
 <span data-ttu-id="38d21-121">**DisplayName** =  _affiche la chaîne_</span><span class="sxs-lookup"><span data-stu-id="38d21-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="38d21-122">**Code** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="38d21-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="38d21-123">**Indicateurs** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="38d21-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="38d21-124">**Attributs** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="38d21-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="38d21-125">Voici un exemple d’un **[verbe.**</span><span class="sxs-lookup"><span data-stu-id="38d21-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="38d21-126">_chaîne_ section **]** .</span><span class="sxs-lookup"><span data-stu-id="38d21-126">_string_ **]** section.</span></span> 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

<span data-ttu-id="38d21-127">Les verbes répertoriés dans cette section sont récupérés par un client à l’aide de la [méthode IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="38d21-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="38d21-128">Verbes sont activés en appelant la méthode du formulaire [IMAPIForm::DoVerb](imapiform-doverb.md) et en lui transmettant le numéro de code de l’action à effectuer.</span><span class="sxs-lookup"><span data-stu-id="38d21-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

