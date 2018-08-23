---
title: Utilisation d’une table pour utiliser les propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f02da9eb1920f55acf65dfb6a503e42d4c3daf2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585422"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="79101-103">Utilisation d’une table pour utiliser les propriétés</span><span class="sxs-lookup"><span data-stu-id="79101-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="79101-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79101-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79101-105">De nombreuses propriétés sont disponibles et à partir des objets qui prennent en charge les colonnes de tables.</span><span class="sxs-lookup"><span data-stu-id="79101-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="79101-106">La mesure du possible, extraire ces propriétés par le biais de la table.</span><span class="sxs-lookup"><span data-stu-id="79101-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="79101-107">Appelez [IMAPITable::SetColumns](imapitable-setcolumns.md) pour inclure toutes les propriétés nécessaires à votre client et [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes de la table.</span><span class="sxs-lookup"><span data-stu-id="79101-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="79101-108">Ces deux appels sont généralement suffisants pour l’extraction de suffisamment d’informations à afficher à l’utilisateur et sont souvent suffisantes pour tout traitement interne nécessaire, un appel à **OpenEntry** pour ouvrir l’objet inutile.</span><span class="sxs-lookup"><span data-stu-id="79101-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="79101-109">Il existe deux exceptions près :</span><span class="sxs-lookup"><span data-stu-id="79101-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="79101-110">Si la propriété est supérieure à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="79101-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="79101-111">Le ** IMAPITable ** interface peut ne pas retourne la valeur de propriété entière, au lieu de cela tronque à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="79101-111">The ** IMAPITable ** interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="79101-112">Pensez à ce compromis, cependant.</span><span class="sxs-lookup"><span data-stu-id="79101-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="79101-113">Si ces données sont affichées à l’utilisateur, 255 octets peut être suffisant pour un champ texte comme un commentaire.</span><span class="sxs-lookup"><span data-stu-id="79101-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="79101-114">Si vous avez besoin d’une propriété spécifique à partir d’une seule ligne dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="79101-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="79101-115">Dans ce cas, il est inutile de créer un tableau avec des propriétés qui ne seront jamais utilisées.</span><span class="sxs-lookup"><span data-stu-id="79101-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="79101-116">Plupart du temps, que vous devez les mêmes propriétés pour toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="79101-116">Most of the time you will need the same properties for all rows.</span></span>
    

