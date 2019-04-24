---
title: Utilisation d'une table pour utiliser les propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329700"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="6b072-103">Utilisation d'une table pour utiliser les propriétés</span><span class="sxs-lookup"><span data-stu-id="6b072-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="6b072-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b072-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b072-105">De nombreuses propriétés sont disponibles à la fois à partir des objets qui les prennent en charge et sous forme de colonnes sur les tableaux.</span><span class="sxs-lookup"><span data-stu-id="6b072-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="6b072-106">Dans la mesure du possible, récupérez ces propriétés via le tableau.</span><span class="sxs-lookup"><span data-stu-id="6b072-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="6b072-107">Appeler [IMAPITable:: SetColumns](imapitable-setcolumns.md) pour inclure toutes les propriétés dont votre client a besoin et la [IMAPITable:: QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes de la table.</span><span class="sxs-lookup"><span data-stu-id="6b072-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="6b072-108">Ces deux appels sont généralement suffisants pour récupérer suffisamment d'informations à l'utilisateur, et sont souvent suffisants pour le traitement interne nécessaire, en effectuant un appel à **OpenEntry** pour ouvrir l'objet.</span><span class="sxs-lookup"><span data-stu-id="6b072-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="6b072-109">Il existe seulement deux exceptions:</span><span class="sxs-lookup"><span data-stu-id="6b072-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="6b072-110">Si la taille de la propriété est de plus de 255 octets.</span><span class="sxs-lookup"><span data-stu-id="6b072-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="6b072-111">L'interface IMAP \* \* ne peut pas retourner la valeur de propriété entière, au lieu de la tronquer à 255 octets.</span><span class="sxs-lookup"><span data-stu-id="6b072-111">The \*\* IMAPITable \*\* interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="6b072-112">Réfléchissez bien à ce compromis.</span><span class="sxs-lookup"><span data-stu-id="6b072-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="6b072-113">Si vous affichez ces données à l'utilisateur, 255 octets peuvent être suffisants pour un champ textuel tel qu'un commentaire.</span><span class="sxs-lookup"><span data-stu-id="6b072-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="6b072-114">Si vous avez besoin d'une propriété spécifique à partir d'une seule ligne dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="6b072-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="6b072-115">Dans ce cas, il n'est pas nécessaire de créer une table avec des propriétés qui ne seront jamais utilisées.</span><span class="sxs-lookup"><span data-stu-id="6b072-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="6b072-116">La plupart du temps, vous aurez besoin des mêmes propriétés pour toutes les lignes.</span><span class="sxs-lookup"><span data-stu-id="6b072-116">Most of the time you will need the same properties for all rows.</span></span>
    

