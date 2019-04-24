---
title: Section [verbes] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327495"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="58e68-103">Section [verbes] du fichier de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="58e68-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="58e68-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58e68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58e68-105">La section **[Verbs]** répertorie l'ensemble complet des verbes pris en charge par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="58e68-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="58e68-106">Le format de la section **[Verbs]** est le suivant:</span><span class="sxs-lookup"><span data-stu-id="58e68-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="58e68-107">**Verbes**</span><span class="sxs-lookup"><span data-stu-id="58e68-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="58e68-108">\*\*\*\* =  _Chaîne_ Verb1</span><span class="sxs-lookup"><span data-stu-id="58e68-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="58e68-109">Voici un exemple de section **[Verbs]** .</span><span class="sxs-lookup"><span data-stu-id="58e68-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="58e68-110">Chaque verbe est défini dans un **verbe [Verb.**</span><span class="sxs-lookup"><span data-stu-id="58e68-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="58e68-111">_String (chaîne_ ) **]** .</span><span class="sxs-lookup"><span data-stu-id="58e68-111">_string_ **]** section.</span></span> <span data-ttu-id="58e68-112">Un **verbe.**</span><span class="sxs-lookup"><span data-stu-id="58e68-112">A **[Verb.**</span></span> <span data-ttu-id="58e68-113">_String (chaîne_ ) **]** décrit un verbe unique offert par le formulaire.</span><span class="sxs-lookup"><span data-stu-id="58e68-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="58e68-114">L'entrée **DisplayName** dans un **verbe [.**</span><span class="sxs-lookup"><span data-stu-id="58e68-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="58e68-115">_String (chaîne_ ) **]** indique le nom de la commande affiché dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58e68-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="58e68-116">L'entrée de **code** correspond au numéro de verbe transmis dans la méthode [IMAPIForm::D overb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="58e68-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="58e68-117">Syntaxe du **verbe [.**</span><span class="sxs-lookup"><span data-stu-id="58e68-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="58e68-118">_String (chaîne_ ) **]** est la suivante:</span><span class="sxs-lookup"><span data-stu-id="58e68-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="58e68-119">**Action.**</span><span class="sxs-lookup"><span data-stu-id="58e68-119">**[Verb.**</span></span> <span data-ttu-id="58e68-120">_String (chaîne_ ) **]**</span><span class="sxs-lookup"><span data-stu-id="58e68-120">_string_ **]**</span></span>
  
 <span data-ttu-id="58e68-121">\*\*\*\* =  _Chaîne affichée_ DisplayName</span><span class="sxs-lookup"><span data-stu-id="58e68-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="58e68-122">\*\*\*\* =  _Entier_ de code</span><span class="sxs-lookup"><span data-stu-id="58e68-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="58e68-123">**Indicateurs** =  de_nombre entier_</span><span class="sxs-lookup"><span data-stu-id="58e68-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="58e68-124">\*\*\*\* =  _Entier_ attribs</span><span class="sxs-lookup"><span data-stu-id="58e68-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="58e68-125">Voici un exemple d'un **verbe [verbe.**</span><span class="sxs-lookup"><span data-stu-id="58e68-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="58e68-126">_String (chaîne_ ) **]** .</span><span class="sxs-lookup"><span data-stu-id="58e68-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="58e68-127">Les verbes répertoriés dans cette section sont récupérés par un client à l'aide de la [méthode IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="58e68-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="58e68-128">Les verbes sont activés en appelant la méthode [IMAPIForm::D overb](imapiform-doverb.md) et en lui transmettant le numéro de code du verbe à effectuer.</span><span class="sxs-lookup"><span data-stu-id="58e68-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

