---
title: Section [extensions] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327299"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="08ace-103">Section [extensions] du fichier de configuration de formulaire</span><span class="sxs-lookup"><span data-stu-id="08ace-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="08ace-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08ace-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08ace-105">La section **[extensions]** répertorie les attributs étendus du formulaire, généralement un jeu de propriétés nommé, qui sont des attributs autres que ceux de base répertoriés dans la section **[Description]** du fichier de configuration de formulaire.</span><span class="sxs-lookup"><span data-stu-id="08ace-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="08ace-106">Les attributs étendus sont des propriétés retournées à partir d'appels à la méthode **GetProps** de l'objet **IMAPIFormInfo** avec le bit supérieur défini dans la balise property.</span><span class="sxs-lookup"><span data-stu-id="08ace-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="08ace-107">Les applications clientes peuvent déterminer les attributs étendus d'un formulaire, le cas échéant, en extrayant ces balises.</span><span class="sxs-lookup"><span data-stu-id="08ace-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="08ace-108">Pour ce faire, les clients appellent la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) , en transmettant les noms des propriétés du formulaire et appellent la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="08ace-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="08ace-109">**Long**</span><span class="sxs-lookup"><span data-stu-id="08ace-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="08ace-110">**Long.**</span><span class="sxs-lookup"><span data-stu-id="08ace-110">**Extension.**</span></span> <span data-ttu-id="08ace-111">_chaîne1_ =  _Chaîne2_</span><span class="sxs-lookup"><span data-stu-id="08ace-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="08ace-112">Chaque section de propriété extension définit un attribut extension à l'aide de la syntaxe de propriété nommée MAPI.</span><span class="sxs-lookup"><span data-stu-id="08ace-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="08ace-113">Le type de propriété doit être PT_LONG ou PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="08ace-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="08ace-114">Les jeux de propriétés qui contiennent des chaînes nommées ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="08ace-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="08ace-115">Le format de la section **[extension]** est le suivant:</span><span class="sxs-lookup"><span data-stu-id="08ace-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="08ace-116">**Long.**</span><span class="sxs-lookup"><span data-stu-id="08ace-116">**[Extension.**</span></span> <span data-ttu-id="08ace-117">_Chaîne2_ **]**</span><span class="sxs-lookup"><span data-stu-id="08ace-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="08ace-118">**Type** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="08ace-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="08ace-119">\*\*\*\* =  _GUID_ NmidPropset</span><span class="sxs-lookup"><span data-stu-id="08ace-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="08ace-120">\*\*\*\* =  _Entier_ NmidInteger</span><span class="sxs-lookup"><span data-stu-id="08ace-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="08ace-121">\*\*\*\* =  __ Chaîne |  de valeur_entière_</span><span class="sxs-lookup"><span data-stu-id="08ace-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="08ace-122">Vous trouverez ci-dessous un exemple de section **[extensions]** et une section associée ultérieure.</span><span class="sxs-lookup"><span data-stu-id="08ace-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


