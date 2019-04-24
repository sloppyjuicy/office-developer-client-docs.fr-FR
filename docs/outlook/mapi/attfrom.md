---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318157"
---
# <a name="attfrom"></a><span data-ttu-id="364d5-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="364d5-103">attFrom</span></span>

<span data-ttu-id="364d5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="364d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="364d5-105">L'attribut **attFrom** est encodé sous la forme d'une structure **TRP** qui encode le nom complet et l'adresse de messagerie de l'expéditeur, suivis du nom complet et de l'adresse de l'expéditeur, suivi de tout remplissage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="364d5-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="364d5-106">Le format de **attFrom** est le suivant:</span><span class="sxs-lookup"><span data-stu-id="364d5-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="364d5-107">**attFrom**: _TRP-structure_ sender-Display-Name _ sender-Address _ Padding</span><span class="sxs-lookup"><span data-stu-id="364d5-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="364d5-108">Sender-Display-Name est une chaîne terminée par un caractère null qui est complétée par un caractère null supplémentaire, si nécessaire, pour atteindre une limite de 2 octets.</span><span class="sxs-lookup"><span data-stu-id="364d5-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="364d5-109">Le remplissage à la fin de l'encodage **attFrom** se compose de autant de caractères nuls que nécessaire pour atteindre une limite **sizeof (TRP)** .</span><span class="sxs-lookup"><span data-stu-id="364d5-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="364d5-110">_TRP:_ **trpidOneOff** cbgrtrp CCH CB</span><span class="sxs-lookup"><span data-stu-id="364d5-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="364d5-111">Pour l'élément **attFrom** , la structure **TRP**est toujours un encodage unique, de sorte que l'trpid du champ **TRP**-structure est toujours **trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="364d5-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="364d5-112">Les éléments cbgrtrp, CCH et CB correspondent aux champs restants de la structure **TRP** .</span><span class="sxs-lookup"><span data-stu-id="364d5-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="364d5-113">Le champ cbgrtrp est calculé comme la somme de **(sizeof (TRP) \*2)**, de la longueur du nom de l'expéditeur-Display-Name par un caractère NULL avec son remplissage, et de la longueur de l'adresse de l'expéditeur-terminé par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="364d5-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="364d5-114">Le champ CCH est calculé comme la longueur du nom complet terminé par un caractère NULL avec son remplissage.</span><span class="sxs-lookup"><span data-stu-id="364d5-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="364d5-115">Le champ CB est calculé comme la longueur de l'adresse de l'expéditeur-terminé par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="364d5-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="364d5-116">_sender-Address:_ Address-type **:** address **' \ 0 '**</span><span class="sxs-lookup"><span data-stu-id="364d5-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="364d5-117">L'adresse de l'expéditeur est une chaîne composée de quatre parties, d'un type d'adresse, d'un signe deux-points (:), de l'adresse proprement dite et d'un caractère de fin null.</span><span class="sxs-lookup"><span data-stu-id="364d5-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="364d5-118">Par exemple, la chaîne `fax:1-909-555-1234\0` doit être une valeur Legal sender-Address.</span><span class="sxs-lookup"><span data-stu-id="364d5-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

