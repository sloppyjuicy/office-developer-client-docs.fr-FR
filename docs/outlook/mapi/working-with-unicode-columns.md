---
title: Utilisation des colonnes Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408382"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="25c8e-103">Utilisation des colonnes Unicode</span><span class="sxs-lookup"><span data-stu-id="25c8e-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="25c8e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25c8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25c8e-105">Les chaînes de caractères dans les tableaux peuvent être représentées à l'aide de caractères standard 8 bits, qui sont des types de propriété PT_STRING8 ou des caractères Unicode 16 bits, dont le type de propriété est PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="25c8e-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="25c8e-106">Les implémenteurs de tableaux sont libres de choisir si leurs tables prennent en charge les chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="25c8e-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="25c8e-107">Étant donné qu'Unicode ajoute de la valeur pour les clients et les fournisseurs de services en étendant le jeu de fonctionnalités, la prise en charge d'Unicode est, autant possible, recommandée.</span><span class="sxs-lookup"><span data-stu-id="25c8e-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="25c8e-108">De nombreuses méthodes de table acceptent un indicateur qui indique si les valeurs de propriété de chaîne sont supposées être Unicode.</span><span class="sxs-lookup"><span data-stu-id="25c8e-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="25c8e-109">Lors de l'entrée, la spécification de l'indicateur MAPI_UNICODE indique à l'implémenteur de tableau que toutes les valeurs de propriété de chaîne transmises avec l'appel sont des chaînes Unicode et ont des types de propriété PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="25c8e-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="25c8e-110">Lors de la sortie, cet indicateur indique que toutes les valeurs de propriété de chaîne renvoyées doivent être des chaînes Unicode, si possible.</span><span class="sxs-lookup"><span data-stu-id="25c8e-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="25c8e-111">Le fait que l'indicateur ait une signification pour l'entrée ou la sortie dépend de la méthode.</span><span class="sxs-lookup"><span data-stu-id="25c8e-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="25c8e-112">Les implémenteurs de tableau qui ne prennent pas en charge Unicode et qui sont transmis à l'indicateur MAPI_UNICODE renvoient la valeur MAPI_E_BAD_CHAR_WIDTH.</span><span class="sxs-lookup"><span data-stu-id="25c8e-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25c8e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25c8e-113">See also</span></span>



[<span data-ttu-id="25c8e-114">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="25c8e-114">MAPI Tables</span></span>](mapi-tables.md)

