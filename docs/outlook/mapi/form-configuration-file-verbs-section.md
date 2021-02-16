---
title: Section Fichier de configuration de formulaire [Verbes]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417783"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="73163-103">Section Fichier de configuration de formulaire [Verbes]</span><span class="sxs-lookup"><span data-stu-id="73163-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="73163-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73163-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73163-105">La section **[Verbes]** répertorie l’ensemble complet des verbes pris en charge par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="73163-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="73163-106">Le format de la section **[Verbes]** est le suivante :</span><span class="sxs-lookup"><span data-stu-id="73163-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="73163-107">**[Verbes]**</span><span class="sxs-lookup"><span data-stu-id="73163-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="73163-108">**Verb1**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="73163-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="73163-109">Voici un exemple de section **[Verbes].**</span><span class="sxs-lookup"><span data-stu-id="73163-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="73163-110">Chaque verbe est défini dans un **[Verbe.**</span><span class="sxs-lookup"><span data-stu-id="73163-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="73163-111">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="73163-111">_string_ **]** section.</span></span> <span data-ttu-id="73163-112">A **[Verbe.**</span><span class="sxs-lookup"><span data-stu-id="73163-112">A **[Verb.**</span></span> <span data-ttu-id="73163-113">_section_ **]** décrit un verbe unique proposé par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="73163-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="73163-114">Entrée **DisplayName** dans un **[Verbe.**</span><span class="sxs-lookup"><span data-stu-id="73163-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="73163-115">_section_ **]** spécifie le nom de la commande affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="73163-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="73163-116">**L’entrée** de code correspond au numéro de verbe transmis dans la méthode [IMAPIForm::D oVerb.](imapiform-doverb.md)</span><span class="sxs-lookup"><span data-stu-id="73163-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="73163-117">Syntaxe du **[Verbe.**</span><span class="sxs-lookup"><span data-stu-id="73163-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="73163-118">_la_ section **string ]** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="73163-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="73163-119">**[Verbe.**</span><span class="sxs-lookup"><span data-stu-id="73163-119">**[Verb.**</span></span> <span data-ttu-id="73163-120">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="73163-120">_string_ **]**</span></span>
  
 <span data-ttu-id="73163-121">**DisplayName**  =   _chaîne affichée_</span><span class="sxs-lookup"><span data-stu-id="73163-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="73163-122">**Code**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="73163-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="73163-123">**Indicateurs**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="73163-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="73163-124">**Attribs**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="73163-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="73163-125">Voici un exemple de **[Verbe.**</span><span class="sxs-lookup"><span data-stu-id="73163-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="73163-126">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="73163-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="73163-127">Les verbes répertoriés dans cette section sont récupérés par un client à l’aide de la méthode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="73163-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="73163-128">Les verbes sont activés en appelant la méthode [IMAPIForm::D oVerb](imapiform-doverb.md) du formulaire et en lui passant le numéro de code du verbe à exécuter.</span><span class="sxs-lookup"><span data-stu-id="73163-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

