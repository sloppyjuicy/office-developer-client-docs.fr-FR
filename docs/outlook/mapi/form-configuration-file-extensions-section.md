---
title: Section [Extensions] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 459c5f5a34421583141028cd9accad5e242d31ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573557"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="99079-103">Section [Extensions] du fichier de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="99079-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="99079-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99079-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99079-105">La section **[Extensions]** répertorie les attributs étendus du formulaire, généralement un ensemble de la propriété nommée, qui sont des attributs au-delà de base celles répertoriées dans la section **[Description]** du fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="99079-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="99079-106">Les attributs étendus sont les propriétés retournées par les appels à la méthode **GetProps** de l’objet **IMAPIFormInfo** avec le bit élevé défini dans la balise de propriété.</span><span class="sxs-lookup"><span data-stu-id="99079-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="99079-107">Les applications clientes peuvent déterminer les attributs étendus d’un formulaire, le cas échéant, en récupérant ces balises.</span><span class="sxs-lookup"><span data-stu-id="99079-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="99079-108">Pour ce faire, les clients appelez la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , en passant les noms des propriétés du formulaire et appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="99079-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="99079-109">**[Extensions]**</span><span class="sxs-lookup"><span data-stu-id="99079-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="99079-110">**Extension.**</span><span class="sxs-lookup"><span data-stu-id="99079-110">**Extension.**</span></span> <span data-ttu-id="99079-111">_la chaîne string1_ =  _chaîne2_</span><span class="sxs-lookup"><span data-stu-id="99079-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="99079-112">Chaque section de la propriété extension définit un attribut d’extension à l’aide de l’interface MAPI nommée la syntaxe de la propriété.</span><span class="sxs-lookup"><span data-stu-id="99079-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="99079-113">Le type de propriété doit être PT_LONG ou PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="99079-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="99079-114">Jeux de propriétés qui contient les chaînes nommées ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="99079-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="99079-115">Le format de la section **[Extension]** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="99079-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="99079-116">**[Extension.**</span><span class="sxs-lookup"><span data-stu-id="99079-116">**[Extension.**</span></span> <span data-ttu-id="99079-117">_chaîne2_ **]**</span><span class="sxs-lookup"><span data-stu-id="99079-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="99079-118">**Type de** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="99079-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="99079-119">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="99079-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="99079-120">**Touche** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="99079-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="99079-121">**Valeur** =  _chaîne_ |  _entier_</span><span class="sxs-lookup"><span data-stu-id="99079-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="99079-122">Voici un exemple d’une section **[Extensions]** et une autre section connexe suivant.</span><span class="sxs-lookup"><span data-stu-id="99079-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


