---
title: Utilisation d’un tableau pour travailler avec des propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439911"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="a4fb3-103">Utilisation d’un tableau pour travailler avec des propriétés</span><span class="sxs-lookup"><span data-stu-id="a4fb3-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="a4fb3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4fb3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4fb3-105">De nombreuses propriétés sont disponibles à la fois à partir des objets qui les prisent en charge et en tant que colonnes sur les tableaux.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="a4fb3-106">Dans la mesure du possible, récupérez ces propriétés par le biais du tableau.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="a4fb3-107">Appelez [IMAPITable::SetColumns](imapitable-setcolumns.md) pour inclure toutes les propriétés dont votre client a besoin et [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="a4fb3-108">Ces deux appels sont généralement suffisants pour récupérer suffisamment d’informations à afficher à un utilisateur et sont souvent suffisants pour tout traitement interne nécessaire, en appelant **OpenEntry** pour ouvrir l’objet inutilement.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="a4fb3-109">Il n’existe que deux exceptions :</span><span class="sxs-lookup"><span data-stu-id="a4fb3-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="a4fb3-110">Si la propriété est de plus de 255 octets.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="a4fb3-111">L’interface \*\* IMAPITable \*\* peut ne pas renvoyer la valeur de la propriété entière, mais la tronquée à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-111">The \*\* IMAPITable \*\* interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="a4fb3-112">Pensez toutefois à ce compromis.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="a4fb3-113">Si vous affichez ces données à l’utilisateur, 255 octets peuvent suffire pour un champ de texte tel qu’un commentaire.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="a4fb3-114">Si vous avez besoin d’une propriété spécifique d’une seule ligne dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="a4fb3-115">Dans ce cas, il est inutile de créer une table avec des propriétés qui ne seront jamais utilisées.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="a4fb3-116">La plupart du temps, vous aurez besoin des mêmes propriétés pour toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="a4fb3-116">Most of the time you will need the same properties for all rows.</span></span>
    

