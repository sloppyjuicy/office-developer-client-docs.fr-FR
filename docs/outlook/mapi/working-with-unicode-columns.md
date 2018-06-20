---
title: Utilisation de colonnes Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9f1fd2d4e4bfdc9ccbbb771fedf1141769c8c8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787467"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="b3cf8-103">Utilisation de colonnes Unicode</span><span class="sxs-lookup"><span data-stu-id="b3cf8-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="b3cf8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3cf8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3cf8-105">Chaînes de caractères dans les tableaux peuvent être représentées à l’aide de caractères 8 bits standard, qui sont de type de propriété PT_STRING8, ou caractères Unicode 16 bits, qui sont du type de la propriété PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b3cf8-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="b3cf8-106">L’implémentation de la table est libres de choisir ou non leurs tables de prise en charge des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="b3cf8-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="b3cf8-107">Étant donné que Unicode ajoute la valeur pour les clients et les fournisseurs de services en étendant le jeu de fonctionnalités, prenant en charge Unicode dans la mesure du possible est recommandée.</span><span class="sxs-lookup"><span data-stu-id="b3cf8-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="b3cf8-108">De nombreuses méthodes de table acceptent un indicateur qui détermine si les valeurs de propriété de chaîne sont supposés être Unicode.</span><span class="sxs-lookup"><span data-stu-id="b3cf8-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="b3cf8-109">À l’entrée, spécifier l’indicateur MAPI_UNICODE indique à l’implémentation de la table que toutes les valeurs de propriété de chaîne transmises avec l’appel sont des chaînes Unicode et dont les types de propriété de PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b3cf8-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="b3cf8-110">Dans la sortie, cet indicateur indique que toutes les valeurs de propriété de chaîne renvoyée doivent être chaînes Unicode, si possible.</span><span class="sxs-lookup"><span data-stu-id="b3cf8-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="b3cf8-111">Si l’indicateur a une signification d’entrée ou de sortie dépend de la méthode.</span><span class="sxs-lookup"><span data-stu-id="b3cf8-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="b3cf8-112">L’implémentation de tableau qui ne prennent pas en charge Unicode et est transmise à l’indicateur MAPI_UNICODE renvoie la valeur MAPI_E_BAD_CHAR_WIDTH.</span><span class="sxs-lookup"><span data-stu-id="b3cf8-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3cf8-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3cf8-113">See also</span></span>



[<span data-ttu-id="b3cf8-114">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="b3cf8-114">MAPI Tables</span></span>](mapi-tables.md)

