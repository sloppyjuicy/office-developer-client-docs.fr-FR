---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432414"
---
# <a name="attfrom"></a><span data-ttu-id="7ee43-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="7ee43-103">attFrom</span></span>

<span data-ttu-id="7ee43-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ee43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ee43-105">**L’attribut attFrom** est codé en tant que structure **TRP** qui encode le nom complet et l’adresse e-mail de l’expéditeur, suivi du nom complet et de l’adresse de l’expéditeur, puis de tout remplissage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7ee43-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="7ee43-106">Le format de **attFrom** est le suivant :</span><span class="sxs-lookup"><span data-stu-id="7ee43-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="7ee43-107">**attFrom**: _TRP-structure_ sender-display-name _ sender-address _ padding</span><span class="sxs-lookup"><span data-stu-id="7ee43-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="7ee43-108">Le nom complet de l’expéditeur est une chaîne terminée par un caractère null qui est ajoutée avec un caractère null supplémentaire, si nécessaire, pour atteindre une limite de 2 byte.</span><span class="sxs-lookup"><span data-stu-id="7ee43-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="7ee43-109">Le remplissage à la fin du codage **attFrom** se compose d’autant de caractères null que nécessaire pour atteindre une limite **sizeof(TRP).**</span><span class="sxs-lookup"><span data-stu-id="7ee43-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="7ee43-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="7ee43-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="7ee43-111">Pour l’élément **attFrom,** la structure **TRP** est toujours un codage unique, donc le trpid hors du champ **TRP**-structure est **toujours trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="7ee43-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="7ee43-112">Les éléments cbgrtrp, cch et cb correspondent aux champs restants de la structure **TRP.**</span><span class="sxs-lookup"><span data-stu-id="7ee43-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="7ee43-113">Le champ cbgrtrp est calculé comme la somme **de (sizeof(TRP) \* 2),** la longueur du nom complet de l’expéditeur terminé par null avec son remplissage et la longueur de l’adresse-expéditeur terminée par null.</span><span class="sxs-lookup"><span data-stu-id="7ee43-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="7ee43-114">Le champ cch est calculé comme la longueur du nom complet terminé par null avec son remplissage.</span><span class="sxs-lookup"><span data-stu-id="7ee43-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="7ee43-115">Le champ cb est calculé comme la longueur de l’adresse-expéditeur terminée par null.</span><span class="sxs-lookup"><span data-stu-id="7ee43-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="7ee43-116">_sender-address:_ address-type **:** address **'\0'**</span><span class="sxs-lookup"><span data-stu-id="7ee43-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="7ee43-117">L’adresse de l’expéditeur est une chaîne composée de quatre parties: le type d’adresse, un deux-points littéral (:), l’adresse elle-même et un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="7ee43-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="7ee43-118">Par exemple, la chaîne `fax:1-909-555-1234\0` serait une valeur d’adresse d’expéditeur légale.</span><span class="sxs-lookup"><span data-stu-id="7ee43-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

