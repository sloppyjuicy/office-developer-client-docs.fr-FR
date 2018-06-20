---
title: Utilisation d’un tableau pour qu’elle fonctionne avec des propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787435"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="135ee-103">Utilisation d’un tableau pour qu’elle fonctionne avec des propriétés</span><span class="sxs-lookup"><span data-stu-id="135ee-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="135ee-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="135ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="135ee-105">De nombreuses propriétés sont disponibles et à partir des objets qui prennent en charge les colonnes de tables.</span><span class="sxs-lookup"><span data-stu-id="135ee-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="135ee-106">La mesure du possible, extraire ces propriétés par le biais de la table.</span><span class="sxs-lookup"><span data-stu-id="135ee-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="135ee-107">Appelez [IMAPITable::SetColumns](imapitable-setcolumns.md) pour inclure toutes les propriétés nécessaires à votre client et [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes de la table.</span><span class="sxs-lookup"><span data-stu-id="135ee-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="135ee-108">Ces deux appels sont généralement suffisants pour l’extraction de suffisamment d’informations à afficher à l’utilisateur et sont souvent suffisantes pour tout traitement interne nécessaire, un appel à **OpenEntry** pour ouvrir l’objet inutile.</span><span class="sxs-lookup"><span data-stu-id="135ee-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="135ee-109">Il existe deux exceptions près :</span><span class="sxs-lookup"><span data-stu-id="135ee-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="135ee-110">Si la propriété est supérieure à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="135ee-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="135ee-111">Le ** IMAPITable ** interface peut ne pas retourne la valeur de propriété entière, au lieu de cela tronque à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="135ee-111">The ** IMAPITable ** interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="135ee-112">Pensez à ce compromis, cependant.</span><span class="sxs-lookup"><span data-stu-id="135ee-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="135ee-113">Si ces données sont affichées à l’utilisateur, 255 octets peut être suffisant pour un champ texte comme un commentaire.</span><span class="sxs-lookup"><span data-stu-id="135ee-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="135ee-114">Si vous avez besoin d’une propriété spécifique à partir d’une seule ligne dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="135ee-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="135ee-115">Dans ce cas, il est inutile de créer un tableau avec des propriétés qui ne seront jamais utilisées.</span><span class="sxs-lookup"><span data-stu-id="135ee-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="135ee-116">Plupart du temps, que vous devez les mêmes propriétés pour toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="135ee-116">Most of the time you will need the same properties for all rows.</span></span>
    

